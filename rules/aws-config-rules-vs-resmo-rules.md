---
description: A list of AWS Config managed rules supported by Resmo
---

# AWS Config Rules vs Resmo Rules

The following table lists managed rules on [AWS Config](https://docs.aws.amazon.com/config/latest/developerguide/managed-rules-by-aws-config.html), supported by Resmo. Mind that the exact queries/rules on Resmo may vary.

| AWS Config Rule                              | Supported by Resmo query/rule |   |
| -------------------------------------------- | ----------------------------- | - |
| ec2-instances-in-vpc                         | Yes                           |   |
| encrypted-volumes                            | Yes                           |   |
| restricted-ssh                               | Yes                           |   |
| autoscaling-group-elb-healthcheck-required   | Yes                           |   |
| autoscaling-launch-config-public-ip-disabled | Yes                           |   |
| cloudfront-associated-with-waf               | Yes                           |   |
| cloudfront-origin-access-identity-enabled    | Yes                           |   |
| cloudfront-origin-failover-enabled           | Yes                           |   |
| dynamodb-table-encrypted-kms                 | Yes                           |   |
| dynamodb-table-encryption-enabled            | Yes                           |   |
| ec2-instance-detailed-monitoring-enabled     | Yes                           |   |
| ec2-instance-multiple-eni-check              | Yes                           |   |
| iam-policy-in-use                            | Yes                           |   |
| iam-user-no-policies-check                   | Yes                           |   |
| iam-user-unused-credentials-check            | Yes                           |   |
| internet-gateway-authorized-vpc-only         | Yes                           |   |
| lambda-dlq-check                             | Yes                           |   |
| lambda-inside-vpc                            | Yes                           |   |
| mfa-enabled-for-iam-console-access           | Yes                           |   |
| multi-region-cloudtrail-enabled              | Yes                           |   |
| opensearch-audit-logging-enabled             | Yes                           |   |
| opensearch-encrypted-at-rest                 | Yes                           |   |
| opensearch-https-required                    | Yes                           |   |
| rds-instance-deletion-protection-enabled     | Yes                           |   |
| rds-instance-iam-authentication-enabled      | Yes                           |   |
| rds-instance-public-access-check             | Yes                           |   |
| s3-bucket-public-read-prohibited             | Yes                           |   |
| s3-bucket-public-write-prohibited            | Yes                           |   |
| s3-bucket-server-side-encryption-enabled     | Yes                           |   |
| s3-bucket-versioning-enabled                 | Yes                           |   |
| vpc-flow-logs-enabled                        | Yes                           |   |

### Support

Find more details on our AWS integration scope and capabilities on the [aws-integration.md](../integrations/aws-integration.md "mention") page. For further inquiries, please contact us via live chat or email us at contact@resmo.com.
