# Security Policy

## Security Contact

For security reports, vulnerability disclosures, suspected abuse, or sensitive implementation concerns, contact:

security@cyberzonic.com

## Sensitive Reporting

Do not open public GitHub issues for vulnerabilities, secrets, customer data, internal architecture, or operational security concerns.

## Repository Security Standard

This repository follows CyberZonic's security-led engineering model:

- No secrets committed to source control
- No .env files committed
- No production credentials in Git history
- No customer or personal data committed
- Least-privilege repository access
- Pull request review for protected branches where supported
- Dependency and supply-chain review before production use
- Security impact considered for all meaningful changes

## Prohibited Content

Do not commit:

- API keys
- Database URLs
- OAuth secrets
- Private keys
- Signing certificates
- Access tokens
- Recovery codes
- Customer data
- Personal data
- Internal incident material
- Production infrastructure credentials