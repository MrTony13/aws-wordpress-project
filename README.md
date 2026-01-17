This project demonstrates how to deploy a production-ready WordPress application on AWS using manual configuration, while following AWS Well-Architected Framework principles — Security, Reliability, Operational Excellence, and Cost Optimization — within the constraints of the AWS Free Tier.

The goal of this project is to simulate a real-world enterprise WordPress deployment, including monitoring, secure credential management, backups, and CDN integration, without using paid services like Application Load Balancers or NAT Gateways.

User → Route 53 → CloudFront (CDN) → EC2 (Apache + PHP + WordPress) → RDS MySQL
                                              ↓
                                       CloudWatch Logs & Metrics
                                              ↓
                                      S3 (Database Backups)


wp-enterprise-manual/
├── README.md
├── ARCHITECTURE.puml
├── docs/
│   ├── deployment_steps.md
│   ├── security_hardening.md
│   └── cloudfront_route53.md
├── scripts/
│   ├── setup_wordpress.sh
│   ├── cloudwatch_install_and_config.sh
│   └── backup_db_to_s3.sh
├── config/
│   ├── cloudwatch-agent-config.json
│   └── wp-config-template.php
└── iam/
    └── ec2_instance_role_policy.json
