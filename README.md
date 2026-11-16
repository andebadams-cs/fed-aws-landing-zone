# fed-aws-landing-zone

A compliance-ready, multi-account AWS landing zone built with Terraform and mapped
to NIST 800-53 controls. It's designed to reflect how federal cloud environments
are secured, logged, and audited.

> In progress. Built as part of my Federal Cloud Engineer roadmap (Oct 2026 – Jul 2027).

## Goals
- Multi-account AWS setup (management, dev, log-archive) with IAM Identity Center
- Secure VPC networking across two Availability Zones
- Encryption, least-privilege IAM, and centralized logging
- NIST 800-53 control mapping (AC, AU, CM, SC families)
- CI/CD with GitHub Actions, OIDC, and security scanning

## Progress

### Phase 1 – Foundations (Oct–Dec 2026)
- [x] AWS Certified Cloud Practitioner (CLF-C02)
- [x] Billing alarms (3 CloudWatch alarms + SNS email alerts) → [write-up](docs/01-billing-alarms.md)
- [x] MFA on root and admin users; AWS Budget
- [ ] Subnet plan: /16 split into public, app, and data subnets across two AZs
- [ ] CompTIA Security+

### Phase 2 – Core Infrastructure
- [ ] Stage 1: AWS Organizations, repo structure, Terraform remote state
- [ ] Stage 2: VPC network module
- [ ] Stage 3: Identity and encryption

### Phase 3 – Security and Compliance
- [ ] Stage 4: Logging and monitoring (CloudTrail, GuardDuty, Security Hub)
- [ ] Stage 5: NIST 800-53 control mapping

### Phase 4 – DevOps
- [ ] CI/CD pipeline with Terraform plan/apply and Checkov scans
- [ ] Automated compliance evidence export

## Cost controls
Billing alarms are set at $5, $25, and $100. I use Free Tier sizes and run
`terraform destroy` after each session.
