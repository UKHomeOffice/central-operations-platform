# Developer Onboarding

This section covers the "how to" for getting a new developer onboarded to our
development systems.

**All COP developers must have SC clearance in place before being given access to the following accounts and systems.**

## 1. Home Office Office 365 accounts

Developers require a Home Office O365 account to access most of the developer
services and tools.

This can be requested by emailing _xxx_. The request must come from COP's
approved requestors.

## 2. GitHub

The developer can add their GitHub account to the UKHomeOffice GitHub
organisation via the Hub's 'Services Onboarding':
https://hub.acp.homeoffice.gov.uk/onboarding/services

Once done, the COP Admins will need to add the developers account to the
`COP Developers` team, which will provide permissions to the COP projects.s

**NOTE: You need to sign all your commits with GPG when pushing your code, please refer to [Managing commit signature verification](https://help.github.com/en/github/authenticating-to-github/managing-commit-signature-verification) and get your account setup before pushing.**

## 3. ACP GitLab

Using their O365 account, the developer needs to log into ACP GitLab:
https://gitlab.digital.homeoffice.gov.uk

Once done, a COP Admin can add the developer to the COP group:
https://gitlab.digital.homeoffice.gov.uk/groups/cop/-/group_members

**NOTE: You need to sign all your commits with GPG when pushing your code, please refer to [Signing commits with GPG](https://docs.gitlab.com/ee/user/project/repository/gpg_signed_commits/) and get your account setup before pushing.**

## 4. COP JIRA and JIRA Service Desk

Using their O365 account, the developer needs to log into COP JIRA:

Once the developer has logged in, they will initially only have access to the
Customer Portal. A COP Admin needs to assign the `COP JIRA user` role in our
Production Keycloak realm. The developer then needs to log out and in again to
inherit the correct permissions via SSO.

## 5. Home Office Slack

Using their O365 account, the developer can create an account at:
https://hod-dsp.slack.com/#/

They then need to be added to the relevant private channels, based on their
role.

## 6. ACP VPNs

Using their O365 account, the developer can log into
https://remote-access.vpn.acp.homeoffice.gov.uk/

For some of the following steps, they must be on the `KUBE-PLATFORM` VPN.

## 7. ACP Hub and Kubernetes clusters

The developer needs to connect to the KUBE-PLATFORM VPN and then log into the
ACP Hub: https://hub.acp.homeoffice.gov.uk/

Once done, a COP Admin can add the developer to the COP project and create
suitable tokens:
https://hub.acp.homeoffice.gov.uk/projects/detail/cop

The developer can follow the guides linked to from the Hub to set up their
Kubernetes access credentials, along with accessing other shared services:

- Kibana
- Drone (GitLab and GitHub)

## 8. ACP Keycloak

When accessing COP Services, the developer will need to log in via Keycloak.
Some services require additional roles to be set in the COP Keycloak realms.

## 9. AWS

Some developers will require AWS credentials. _TBC_

## x. Home Office Confluence

_TBC_

## x. Other COP services

### x.y Camunda

### x.y Formbuilder

### x.y Matomo
