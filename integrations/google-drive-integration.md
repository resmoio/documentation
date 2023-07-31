---
description: Guide for Resmo Google Drive integration
---

# Google Drive Integration

## Resmo + Google Drive Integration Fundamentals

<figure><img src="../.gitbook/assets/google-drive-logo.png" alt=""><figcaption></figcaption></figure>

Resmo integrates with Google Drive in one click to bring visibility and security to your Google Drive environment.

### What does Resmo offer to Google Drive users?

* Collect any kind of documents from your Drive.
* Query your documents to see scopes and visibilities.
* Set up custom security rules and run custom SQL queries to improve asset visibility.
* Use managed queries to evaluate your Google Drive security quickly.
* Understand how your Drive assets relate to each other in graph view.

### How does the integration work?

Resmo uses Google Workspace Reports API to do the initial polling and collect existing resources. Following the initial polling, it receives events in real time through webhook.

#### **Available resources**

{% embed url="https://resources.resmo.com/googledrive" %}

{% hint style="warning" %}
**Critical Notes**

* Business Standard pricing plan required at least one Google Workspace account to run this integration successfully.
* We are not accessing your document's content. Google Drive integration only takes permission for audit logs and customer information.
* Initially, this integration polls the last six months' audit logs, creates document resources, and listens for document events.
{% endhint %}

## Integration walkthrough

### How to install

1. Log in to your Resmo account and go to the Integrations page.
2. From there, select Google Drive and click the Add Integration button from the bottom right corner of the opening modal.

<figure><img src="../.gitbook/assets/add-google-drive.png" alt=""><figcaption></figcaption></figure>

5\. Hit the Create button, and you'll be redirected to your Google Account. Accept permissions.

6\. Your Google Drive integration is ready! Now you can start querying your resources!

<figure><img src="../.gitbook/assets/google-drive-security-queries.png" alt=""><figcaption></figcaption></figure>

### How to uninstall

1. Go to your Integrations page on Resmo.
2. Select Google Drive and go to the Integrated Accounts tab on the opening modal. Select the account you want to remove.
3. For temporary disabling, click the **Disable** button from the top right. This action can be reversed later by enabling the integration back. Or you can permanently uninstall the integration by clicking the **Delete** button. This action cannot be undone.

<figure><img src="../.gitbook/assets/googledrive-disable.png" alt=""><figcaption></figcaption></figure>
