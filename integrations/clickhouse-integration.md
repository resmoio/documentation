---
description: Guide for Resmo ClickHouse integration
---

# ClickHouse Integration

<figure><img src="../.gitbook/assets/clickhouse-logo.png" alt=""><figcaption></figcaption></figure>

Resmo seamlessly integrates with ClickHouse, allowing you to effortlessly collect directory assets such as users, schemas, and tables from your ClickHouse database. It empowers you with the ability to query ClickHouse users, schemas, tables, and more while also providing the flexibility to establish custom rules and execute custom SQL queries, ultimately enhancing asset visibility and ensuring a safe and compliant ClickHouse environment.

### What does Resmo offer to ClickHouse users?

* Collect your directory assets like users, schemas, and tables from your ClickHouse database.
* Ability to query your ClickHouse users, schemas, tables, and much more.
* Set up custom rules and run custom SQL queries to improve asset visibility.

### How does the integration work?

Resmo ClickHouse Integration collects resources by using our database agent. After you create, integrate, and set the configurations specified in the How to Install section, the database agent starts operating. Once triggered, it sends requests to our servers, pulling resources inside the database.&#x20;

Then, we process them on the server. You can use the database agent as a binary or docker image, depending on your chosen installation path. Resmo performs the resource validation with a unique IngestKey. Note: An IngestKey is different for each integration.

**Available resources:**

{% embed url="https://resources.resmo.com/clickhouse" %}

### Integration Walkthrough

#### How to install

1. Login to your Resmo account and navigate to the Integrations page. Then, find and click ClickHouse.
2. Click the **Add Integration** button from the bottom right corner of the opening modal.

<figure><img src="../.gitbook/assets/add-clickhouse.png" alt=""><figcaption></figcaption></figure>

3. Copy and paste your **ClickHouse ingest key** (Ingest Key is used as a secret for authentication).

<figure><img src="../.gitbook/assets/clickhouse-ingest-key.png" alt=""><figcaption></figcaption></figure>

4. Hit the Create button.
5. Go to [Resmo-Database-Agent](https://github.com/resmoio/resmo-database-agent).

<figure><img src="../.gitbook/assets/resmo-agent.png" alt=""><figcaption></figcaption></figure>

6. Click on "tags".
7. If you want to binary version, click on the desired OS version of the Resmo Database Agent.
8. After downloading, you can run the database agent by providing the config values.
9. Config list:
   * **IngestKey:** Ingest key of your integration. (Required)
   * **DSN:** Database connection URL (Required). We expect the URL to follow a specific format starting with "clickhouse://...".
   * **Schedule:** Schedule for running queries(Optional)
   * **Timeout:** Timeout duration for database connections, ingesting etc. (Optional, 10 seconds default)
   * **DbIdentifier:** Database identifier for related Resmo resources.
10. You can run database runner for the binary version with commands:
    * `` `./resmo-database-agent -ingestKey="d1f947fa-f585-11ed-b67e-0242ac120002" -dsn="clickhouse://resmo:resmo@localhost:8123" -schedule="10m" -timeout="10s" -dbIdentifier="clickhouse-prod"` `` or:
    * `` `INGEST_KEY="d1f947fa-f585-11ed-b67e-0242ac120002" DSN="clickhouse://resmo:resmo@localhost:8123" ./resmo-database-agent` ``
11. Or you can use the docker version via command:
    * `` `docker pull ghcr.io/resmoio/resmo-database-agent:latest` ``
    * `` `docker run ghcr.io/resmoio/resmo-database-agent -ingestKey="d1f947fa-f585-11ed-b67e-0242ac120002" -dsn="clickhouse://resmo:resmo@localhost:8123" -schedule="10m" -timeout="10s" -dbIdentifier="clickhouse-prod"` `` or:
      * `` `docker run -e DSN="clickhouse://resmo:resmo@localhost:8123" -e RESMO_INGEST_KEY="d1f947fa-f585-11ed-b67e-0242ac120002" /resmo-database-agent` ``
12. You are ready! Now you can start querying your ClickHouse database resources!

#### How to uninstall

1. Go to your Integrations page on Resmo and click on ClickHouse.
2. Navigate to the Connected Integrations tab on the opening modal.
3. Select the ClickHouse account you want to remove or disable. Click the Disable/Delete button from the top right of the modal.&#x20;

Note that account removal cannot be undone; you would need to integrate again. Instead, you can choose to disable an integration until you enable it back.

<figure><img src="../.gitbook/assets/uninstall-clickhouse.png" alt=""><figcaption></figcaption></figure>
