---
description: A glossary of key concepts and terminology used throughout Resmo
---

# Glossary

### Account & User

A user and an account are automatically created after signup.&#x20;

Learn more about accounts: [accounts.md](../settings/accounts.md "mention")

Learn more about users: [user.md](../users-and-permissions/user.md "mention")

### Integration

Integration is used to feed the required data for Resmo to do its job. They are easy to integrate and secure by default.

Learn more about integrations: [integrations-guide.md](../integrations/integrations-guide.md "mention")

### Resource

Resources are entities created, updated or deleted in integration tools. &#x20;

Asset and resource keywords are used interchangeably. Resmo collects a resource's configuration, not the data itself.&#x20;

For example, an Amazon EC2 instance has a resource like this in Resmo:

```json
{ 
    accountId:"935339171232" 
    amiId:"ami-372gd78g23rc1" 
    availabilityZone:"eu-central-1a" 
    instanceId:"i-1b9f37t81aec3a631" 
    instanceType:"t2.nano" 
    name:"application-server" 
    networkInterfaces:[] 
    publicIp:null 
    region:"eu-central-1" 
    state:"running" 
    subnetId:"subnet-2310d721" 
    tags:{}
}
```

Each resource has an associated key and configuration data:

* Key
  * ie. GitHub has repositories or users which you can access using _github\_repository_ and _github\_user keys in Resmo._
* Configuration data - in JSON format
  * See the EC2 example above.

Learn more about resources: [resources.md](../resources/resources.md "mention")

### Query

Users can query resources using SQL. Our SQL interface is powerful and easy to get started. Resmo offers ready-to-use queries for all integrations. Users can also write their own queries, save and share them with others.

Learn more about queries: [Broken link](broken-reference "mention")&#x20;

### Resource Group

Resource groups are used to organize Resmo resources. They are used to view, filter, manage resources easily.&#x20;

Common use-cases for resource groups:&#x20;

* development, staging and production environments
* accounts
* teams

Learn more about resource groups: [resource-groups.md](../resource-tags/resource-groups.md "mention")

### Rule

Rules represent desired states for resources. They are used to evaluate resource's configuration data against specified settings. Resmo offers managed rules (predefined) and custom rules (customizable). Rule notifications can notify users as soon as a violation happen.

ie. Ensure IAM password policy prevents password reuse.

Learn more about rules: [Broken link](broken-reference "mention")

### Pack

Packs are used to group rules. They offer ready-to-use templates for common best practices and compliance frameworks.

Learn more about conformance packs: [Broken link](broken-reference "mention")

### Notification

Notifications are used to notify users. Resmo supports many notification channels like e-mail, webhook, Slack, Opsgenie and more. Customers can receive real-time or regular updates via notifications.

Learn more about notification: [notification-channels.md](../notifications/notification-channels.md "mention")&#x20;
