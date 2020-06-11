# Developer Onboarding

This section covers the "how to" for getting a new developer onboarded to our
development systems.

**All COP developers must have SC clearance in place before being given access
to the following accounts and systems.**


## 1. Home Office Office 365 accounts

Developers require a Home Office O365 account to access most of the developer
services and tools.

This can be requested by emailing *xxx*. The request must come from COP's
approved requestors.

## 2. ACP GitLab

Using their O365 account, the developer needs to log into ACP GitLab:
https://gitlab.digital.homeoffice.gov.uk

Once done, a COP Admin can add the developer to the COP group:
https://gitlab.digital.homeoffice.gov.uk/groups/cop/-/group_members


## 3. COP JIRA and JIRA Service Desk

Using their O365 account, the developer needs to log into COP JIRA:

Once the developer has logged in, they will initially only have access to the
Customer Portal. A COP Admin needs to assign the `COP JIRA user` role in our
Production Keycloak realm. The developer then needs to log out and in again to
inherit the correct permissions via SSO.


## 4. Home Office Slack

Using their O365 account, the developer can create an account at:
https://hod-dsp.slack.com/#/

They then need to be added to the relevant private channels, based on their
role.


## 5. ACP VPNs

Using their O365 account, the developer can log into
https://remote-access.vpn.acp.homeoffice.gov.uk/

For some of the following steps, they must be on the `KUBE-PLATFORM` VPN.


## 6. ACP Hub and Kubernetes clusters

The developer needs to connect to the KUBE-PLATFORM VPN and then log into the
ACP Hub: https://hub.acp.homeoffice.gov.uk/

Once done, a COP Admin can add the developer to the COP project and create
suitable tokens:
https://hub.acp.homeoffice.gov.uk/projects/detail/cop

The developer can follow the guides linked to from the Hub to set up their
Kubernetes access credentials, along with accessing other shared services:

* Kibana
* Drone (GitLab and GitHub)

## 7. GitHub

The developer can add their GitHub account to the UKHomeOffice GitHub
organisation via the Hub's 'Services Onboarding':
https://hub.acp.homeoffice.gov.uk/onboarding/services

Once done, the COP Admins will need to add the developers account to the
`COP Developers` team, which will provide permissions to the COP projects.s

## 8. ACP Keycloak

When accessing COP Services, the developer will need to log in via Keycloak.
Some services require additional roles to be set in the COP Keycloak realms.


## 8. AWS

Some developers will require AWS credentials. *TBC*


## x. Home Office Confluence

*TBC*

## x. Other COP services

### x.y Camunda

### x.y Formbuilder

### x.y Matomo
