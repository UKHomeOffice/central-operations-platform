# Product Engineering

*Product Engineering team to add content*

## Agile Process

*[Tom F to write]*

## User Experience (UX)

*[Tom C to write, with input from Andrew]*

### UX Research

*[Tom C to write, with input from Andrew]*

### Assisted Digital

*[Tom C to write, with input from Andrew]*

### Interaction Design

*[Tom C to write, with input from Andrew]*

### Content Design

*[Tom C to write, with input from Andrew]*

## Software Engineering

Our software engineering practices are focused on turning the designs and ideas
generated through user research into stable and performant products, that our
users can access reliably and securely.

### CI/CD Process

All of our deployments are run from our CI/CD pipelines, run using
[Drone](https://drone.io/).

We have integrated linting, testing and test coverage into our CI/CD pipelines
ahead of deploying changes to our environments.

## Infrastructure Engineering

We deploy our products using a combination of Kubernetes, AWS and Azure
resources.

### Kubernetes

We manage our Kubernetes resources using a custom Kubernetes resources
deployment tool called [kd](https://github.com/UKHomeOffice/kd).

This allows us to template our deployments so that the templates can be applied
in each of our environments with only the environment variables being changed.
This provides us with high levels of assurance that our Production and
development environments are consistent.

### AWS

We manage our AWS resources using Terraform.

*[Belinda to add some more info]*

### Azure

*[Update required on how we are managing Azure resources]*

## Quality Assurance

*[Rohit to write/contribute to]*

## Security

We take a *Secure by Design* approach and ensure that building secure systems is
a theme throughout our software engineering lifecycle.

Our primary security practices include:

- Security specialists are embedded in our team
- All code must be committed from an authorised and verified account (using GPG signed commits)
- Regular IT Health Checks (ITHC) conducted by an independent third-party

For more information, please refer to our Security documentation [link required], specifically the following documents:

- Central Operations Platform Administration Security Operating Procedures [link required]

## Tooling

Our Product Engineering team uses a wide range of tools to build COP products.

### Accounts

To develop COP products you will have the following accounts:

- Microsoft O365 accounts (centralised account management)
- GitHub (for open source projects)

The O365 accounts govern access to:
- GitLab (for closed source projects)
- Keycloak (for role-based access)
- COP JIRA and JIRA Service Desk (for development tickets and incident management)
- ACP Hub and Kubernetes clusters
- VPNs
- Matomo (for web analytics)
- Home Office Confluence

### Developer Onboarding Process

For developer onboarding, please follow our [guide](developer-onboarding.md)
