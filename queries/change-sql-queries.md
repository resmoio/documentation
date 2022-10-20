# Change SQL Queries

Resmo keeps track of changes to resources and you can query them using SQL like regular resources. For example, you want to see your GitHub repositories and you run a query:

`SELECT * FROM github_repo`

When you want to see changes made to your repositories over time, you can run a query like:

{% hint style="info" %}
`SELECT * FROM github_repo_changes`
{% endhint %}

This _\_change_ query is available for all resources like `aws_s3_bucket_changes`.

Take a look at [resource-changes.md](../resources/resource-changes.md "mention") documentation to learn more about the fields returned.

Sample query from the managed Resmo queries:

![](<../.gitbook/assets/Screen Shot 2022-05-25 at 21.16.31.png>)

