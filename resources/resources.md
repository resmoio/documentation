---
description: Overview of Resmo resources.
---

# Resources

Resources are entities in integration tools. They are created, updated or deleted, meaning they have "changes". Sample resources are Amazon EC2 instances, Amazon S3 buckets, GitHub Repositories or Slack users.

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

### Resource Anatomy

Each resource has an associated key and configuration data:

* Key
  * ie. GitHub has repositories or users which you can access using _github\_repository_ and _github\_user keys in Resmo._
  * _Keys are singular._
  * Keys follow the integration key + service name + entity name standard. ie. _aws\_s3\_bucket_. If the integration is the service itself, it becomes integration name + entity name. ie. _github\_repository_ or _slack\_channel._
* Configuration data - in JSON format
  * See the EC2 example above.

Each resource has also changes and they are also available to query. See [resource-changes.md](resource-changes.md "mention")

### Resource Collection

Resources are collected via integrations. Integrations offer different collection methods. Check out  the [integrations-guide.md](../integrations/integrations-guide.md "mention") for more information.

### Resource Fields

Each resource has meta object for Resmo related data. At the same level as meta, we write the actual resource object.

Resources have the following field structure:

```json
_meta: {
  event: { -> event's 
    "actor": Any, -> can be a username or an object, depending on the integration
     "type": "renamed",
     "payload": Any -> event's payload
  },
  integration: {
    "id": "",
     "name": "",
     "tags": ["",""]
  },
  resource: "github_repo",
  recordedAt: date,
},
... -> the rest is resource's content
```

### All Collected Resources

Resmo has more than 200 resources collected in near-real-time and the number is increasing every day. If you want to see all of them take a look at TBA.

