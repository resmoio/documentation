---
description: Getting started with SQL queries in Resmo
---

# Standard SQL Queries

SQL is a well-known and powerful language. Resmo users can query their resources and changes using standard SQL statements with auto-complete support.

![](<../.gitbook/assets/Screen Shot 2022-05-18 at 16.38.01.png>)

### Query examples

All SQL queries are standard _`Select`_ statements.&#x20;

**Simple SQL query**

{% hint style="info" %}
**List all Jira users**

`SELECT * FROM jira_user`
{% endhint %}

#### SQL query with where clause

{% hint style="info" %}
**List all active Jira users**

`SELECT accountId, displayName, emailAddress FROM jira_user WHERE active = true AND accountType = 'atlassian'`
{% endhint %}

#### SQL query with Group By clause

![](<../.gitbook/assets/Screen Shot 2022-05-18 at 22.01.44.png>)

{% hint style="info" %}
**Jira users per group**

`SELECT g, COUNT(*) FROM jira_user u, u.groups g GROUP BY gSimple SQL query with where statement`
{% endhint %}

**SQL query with IN statement to run cross resource queries**

{% hint style="info" %}
**NewRelic users that don’t exist on Google Workspace**

`SELECT name, email FROM newrelic_user WHERE email NOT IN (SELECT VALUE primaryEmail FROM gsuite_user)`
{% endhint %}

**SQL query response filtered for a field in an object**

Print aliasTager's dnsName:

{% hint style="info" %}
SELECT accountId,accountName,hostedZoneName,name, **aliasTarget.dnsName** FROM aws\_route53\_hosted\_zone\_record
{% endhint %}

**SQL query with nested objects**

Most configuration data is nested and it's easy to refer to inner objects with the dot notation.&#x20;

{% hint style="info" %}
SELECT metadata.namespace, metadata.name FROM kubernetes\_replicaset r, r.spec.template.spec.containers container
{% endhint %}

### Functions

Functions help simplify queries that are hard to write.&#x20;

The following function with `aws_sg_allows` function shortens the SQL query a lot.

{% hint style="info" %}
`SELECT accountId, region, vpcId, name, description FROM aws_vpc_security_group WHERE aws_sg_allows(ingress, '0.0.0.0', 25, 3389)`
{% endhint %}

The following functions are available at the moment:

* TBA

### Supported SQL keywords

All standard keywords supported in Select SQL queries are available to use.&#x20;

Some common keywords are:

* DISTINCT
* SUM
* COUNT
* COALESCE

### Reserved Keywords

<details>

<summary>Keyword list</summary>

"absolute", "action", "add", "all", "allocate", "alter", "and", "any", "are", "as", "asc", "assertion", "at", "authorization", "avg", "begin", "between", "bit", "bit\_length", "by", "cascade", "cascaded", "case", "cast", "catalog", "char", "character", "character\_length", "char\_length", "check", "close", "coalesce", "collate", "collation", "column", "commit", "connect", "connection", "constraint", "constraints", "continue", "convert", "corresponding", "count", "create", "cross", "current", "current\_date", "current\_time", "current\_timestamp", "current\_user", "cursor", "date", "deallocate", "dec", "decimal", "declare", "default", "deferrable", "deferred", "delete", "desc", "describe", "descriptor", "diagnostics", "disconnect", "distinct", "domain", "double", "drop", "else", "end", "end-exec", "escape", "except", "exception", "exec", "execute", "exists", "external", "extract", "date\_add", "date\_diff", "false", "fetch", "first", "float", "for", "foreign", "found", "from", "full", "get", "global", "go", "goto", "grant", "group", "having", "identity", "immediate", "in", "indicator", "initially", "inner", "input", "insensitive", "insert", "int", "integer", "intersect", "interval", "into", "is", "isolation", "join", "key", "language", "last", "left", "level", "like", "local", "lower", "match", "max", "min", "module", "names", "national", "natural", "nchar", "next", "no", "not", "null", "nullif", "coalesce", "numeric", "octet\_length", "of", "on", "only", "open", "option", "or", "order", "outer", "output", "overlaps", "pad", "partial", "position", "precision", "prepare", "preserve", "primary", "prior", "privileges", "procedure", "public", "read", "real", "references", "relative", "restrict", "revoke", "right", "rollback", "rows", "schema", "scroll", "section", "select", "session", "session\_user", "set", "size", "smallint", "some", "space", "sql", "sqlcode", "sqlerror", "sqlstate", "substring", "sum", "system\_user", "table", "temporary", "then", "time", "timestamp", "to", "transaction", "translate", "translation", "trim", "true", "union", "unique", "unknown", "update", "upper", "usage", "user", "using", "value", "values", "varchar", "varying", "view", "when", "whenever", "where", "with", "work", "write", "zone"

</details>
