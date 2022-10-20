---
description: View and debug resources and its changes using SQL.
---

# Query Types

Resmo resources and resource changes can be queried using SQL (Learn more [standard-sql-queries.md](standard-sql-queries.md "mention")). Queries are fundamental constructs used in multiple places. They help:

* Get visibility into resources and their changes
* Group and get insights from different tools
* See aggregate information with grouping
* Run analysis in Rules ( [Broken link](broken-reference "mention"))

## Free Form Queries

Users can run free from queries on the search page.&#x20;

Rules also contain queries, either free form or saved queries.

A sample query that would list name, AWS region and account id information for not encrypted SQS queues.

{% code title="List not encrypted Amazon SQS queues" %}
```sql
SELECT name, region, accountId FROM aws_sqs_queue WHERE kmsMasterKeyId IS NULL
```
{% endcode %}

## Saved Queries

Saved Queries are accessible via the Queries page and can be referenced in Rules.

### Managed Queries

These are queries managed by our team. Once you sign up and integrate Resmo with your tools, you can immediately run these queries against your resources and gain insights.

![](<../.gitbook/assets/Screen Shot 2022-05-23 at 18.38.40.png>)

### Custom Queries

Customers can save their own queries and access them from a simple UI.&#x20;

## Query History

Resmo keeps track of every executed query. Users can reach their query history for easy access from the search page.&#x20;

They can only see their own query execution history while admins can see all executed queries.

![](<../.gitbook/assets/Screen Shot 2022-05-23 at 18.37.47.png>)
