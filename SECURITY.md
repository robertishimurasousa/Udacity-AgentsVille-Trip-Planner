# Security Policy

## Reporting a vulnerability

Use **Report a vulnerability** from the repository's [Security tab](https://github.com/robertishimurasousa/Udacity-AgentsVille-Trip-Planner/security) to contact the maintainer privately. Describe the affected revision, the observed behavior, and the impact. Use synthetic data and omit credentials from reports and attachments.

## Handling credentials

Store the API key in the ignored local `.env` or in the notebook process environment. Use a blank value in `.env.example`. Review notebook source, outputs, and metadata for sensitive data before sharing them. If a key is exposed, revoke or rotate it with the issuer and report the exposure privately.
