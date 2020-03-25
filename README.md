# Central Operations Platform Handbook

This project is the Home Office's Central Operations Platform (COP) team's
handbook.

You can view the live handbook [here](https://ukhomeoffice.github.io/central-operations-platform/).

It is inspired by GitLab's [Handbook](https://about.gitlab.com/handbook/).

## How to contribute

**[TO DO]** Contribution guide

### Building locally

This project require Python 3 to build.

```
python3 -m venv cop-docs
source cop-docs/bin/activate
pip install mkdocs mkdocs-material markdown-include
mkdocs build
```

## Configuring the deployment

This repository requires a single secret in Drone, the GitHub deploy key. This
should be a regular SSH certificate pair.

### Generate the certificates

Run:

```
ssh-keygen -t rsa -b 4096 -C "<COP support email>"
```

**Do not set a password** for the certificate (as per https://developer.github.com/v3/guides/managing-deploy-keys/#deploy-keys)
 otherwise the deployment will fail.

### Adding the deploy key to GitHub

GitHub needs to have the **public key** added as a Deploy Key **with write access**.

This can be added at: [Settings > Deploy Keys](https://github.com/UKHomeOffice/central-operations-platform/settings/keys)

### Adding the private key to drone

Drone needs the **private key** to identify itself to GitHub (using the deploy key)
and this should be provided as a Drone secret called `SSH_KEY`.
