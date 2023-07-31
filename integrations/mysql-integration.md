---
description: Guide for Resmo MySQL integration
---

# MySQL Integration

<figure><img src="../.gitbook/assets/mysql-logo_.png" alt=""><figcaption></figcaption></figure>

Resmo seamlessly integrates with MySQL, providing comprehensive visibility and ensuring the safety and compliance of your MySQL environment.

### What does Resmo offer to MySQL users?

* Collect your directory assets like users, schemas, and tables from your MySQL database.
* Ability to query your MySQL users, schemas, tables, and much more.
* Set up custom rules and run custom SQL queries to improve asset visibility.

### How does the integration work?

Resmo MySQL Integration collects resources by using our database agent. After you create and integrate and set the configurations as specified in the [How to Install section](mysql-integration.md#how-to-install), the database agent starts to operate. Once triggered, it sends requests to our servers, pulling resources inside the database.&#x20;

Then, we process them on the server. You can use the database agent as a binary or docker image, depending on the installation path you choose. Resmo performs the resource validation with a unique IngestKey. Note: An IngestKey is different for each integration.

**Available resources:**

{% embed url="https://resources.resmo.com/mysql" %}

### Integration Walkthrough

#### How to install

1. Login to your Resmo account and navigate to the Integrations page. Then, find and click MySQL.
2. Click the **Add Integration** button from the bottom right corner of the opening modal.

<figure><img src="../.gitbook/assets/add-mysql.png" alt=""><figcaption></figcaption></figure>

3. Copy and paste your MySQL ingest key (Ingest Key is used as a secret for authentication).

<figure><img src="../.gitbook/assets/mysql-ingest-key.png" alt=""><figcaption></figcaption></figure>

4. Hit the Create button.
5. Go to [Resmo-Database-Agent](https://github.com/resmoio/resmo-database-agent).

<figure><img src="../.gitbook/assets/resmo-agent.png" alt=""><figcaption></figcaption></figure>

6. Click on "tags."
7. If you want to binary version, click on the desired OS version of the Resmo Database Agent.
8. After downloading, you can run the database agent by providing the config values.
9. Config list:
   * **IngestKey:** Ingest key of your integration. (Required)
   * **DSN:** Database connection URL (Required). We expect the URL to follow a specific format starting with "mysql://...".
   * **Schedule:** Schedule for running queries(Optional)
   * **Timeout:** Timeout duration for database connections, ingesting etc. (Optional, 10 seconds default)
   * **DbIdentifier:** Database identifier for related Resmo resources.
10. You can run database runner for the binary version with commands:
    * `` `./resmo-database-agent -ingestKey="d1f947fa-f585-11ed-b67e-0242ac120002" -dsn="mysql://resmo:resmo@localhost:3306" -schedule="10m" -timeout="10s" -dbIdentifier="mysql-prod"` `` or:
    * `` `INGEST_KEY="d1f947fa-f585-11ed-b67e-0242ac120002" DSN="mysql://resmo:resmo@localhost:3306" ./resmo-database-agent` ``
11. Or you can use the docker version via command:
    * `` `docker pull ghcr.io/resmoio/resmo-database-agent:latest` ``
    * \``` docker run ghcr.io/resmoio/resmo-database-agent -ingestKey="d1f947fa-f585-11ed-b67e-0242ac120002" -dsn="mysql://resmo:resmo@localhost:3306" -schedule="10m" -timeout="10s" -dbIdentifier="mysql-prod"` `` or:
      * `` `docker run -e DSN="mysql://resmo:resmo@localhost:3306" -e INGEST_KEY="d1f947fa-f585-11ed-b67e-0242ac120002" /resmo-database-agent` ``
12. You are ready! Now you can start querying your MySQL database resources!

#### How to uninstall

1. Go to your Integrations page on Resmo and click on MySQL.
2. Navigate to the Connected Integrations tab on the opening modal.
3. Select the MySQL account you want to remove or disable. Click the Disable/Delete button from the top right of the modal.&#x20;

Note that account removal cannot be undone; you would need to integrate again. Instead, you can choose to disable an integration until you enable it back.

<figure><img src="../.gitbook/assets/delete-disable-mysql.png" alt=""><figcaption></figcaption></figure>
