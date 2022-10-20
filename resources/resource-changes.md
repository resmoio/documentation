---
description: Overview of Resmo resource changes.
---

# Resource Changes

Each resource has changes over time. They are created, updated or deleted. Customers can query these changes. They can use them in saved queries and rules.

{% hint style="info" %}
ie. _github\_repository_ resources has changes __ available at _github\_repository\_changes_ key __ while _jira\_user_ resources has changes available at _jira\_user\_changes_.
{% endhint %}

Changes are powerful because they provide context on a resource's life cycle. Some use-cases:

* See who caused the change (available for some resources)

### Resource Change Types

There are three types of changes

* added
* modified
* removed

### Resource Change Fields

Each resource has changes and users can query them by adding "changes" at the end of the resource's name. For example, for github\_repository resource, the changes are kept at github\_repository\_changes.

Resource changes have the following field structure:

```json
_meta: {
  id: String,
  groupKey: String,
  integration: {
    "id": String,
     "name": String,
     "tags": String Array | null,
  },
  type: String -> "github_repo",
  recordId: date,
  recordedAt: date,
},
resourceId: "", -> internally generated id for changes of a resource 
recordedAt: date,
type: String -> "added | modified | removed",
actor: Object | null,
eventType: Sting | null, -> event type like "repository/privatized"
fields: Array | null,
after: { 
     -> resource's content before after it changes
 },
before: { 
     -> resource's content before it changes, null if this is resource's first change
}
}
```

### Resource Change View

You can also visually see changes under /resources directory for each resource.

![](<../.gitbook/assets/Screen Shot 2022-05-25 at 10.15.07.png>)
