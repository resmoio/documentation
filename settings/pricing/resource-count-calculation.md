# Resource Count Calculation

The Professional pricing plan covers 20,000 resources. Once this limit is exceeded, Resmo charges an additional $89 per 2,000 extra resources. This calculation is based on usage-metered pricing, which will sum up the monthly average of your resource usage and add the additional charge depending on your resource count.

(daily average usage - capability) / day

The following resource types have different multipliers when calculating your resource count.

### Resource Multiplier (Tokenizing resources)

A resource, like an Slack user or an S3 bucket counts as 1 resource unless otherwise specified. By multiplying the number of resources we charge, we reduce the number of resources we charge for default (comes with the integration - usually not created by the users like aws\_region) or more frequent resources.

| **ResourceType**         | **Multiplier** |
| ------------------------ | -------------- |
| `aws_iam_managed_policy` | 0.1            |
| aws\_region              | 0.1            |
| datadog\_permission      | 0.1            |
| `flyio_region`           | 0.1            |
| `gcp_iam_role`           | 0.1            |
| `googledrive_document`   | 0.05           |

**For example,** for the following resource types and counts:

| **Resource Type**         | **Resource Count** | **Multiplier** |
| ------------------------- | ------------------ | -------------- |
| aws\_account              | 100                | 1              |
| aws\_managed\_iam\_policy | 1000               | 0.1            |
| google\_drive\_document   | 10000              | 0.05           |

The resource count will be calculated as follows:

* aws\_account: 100 \* 1 = 100
* aws\_managed\_iam\_policy: 1000 \* 0.1 = 100
* google\_drive\_document: 10.000 \* 0.05 = 500
* daily total usage will be: 100 + 100 + 500 = 700

### Support

Contact us via live chat or email us at contact@resmo.com for feedback or additional queries.\
