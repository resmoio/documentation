---
description: Guide for Resmo Brex Integration
---

# Brex Integration

## Resmo + Brex Integration Fundamentals

<figure><img src="../.gitbook/assets/brex-logo.png" alt=""><figcaption></figcaption></figure>

Resmo Brex integration helps you gain visibility over your Brex resources, like companies, departments, and users, while keeping your environment secure and compliant.

### What does Resmo offer to Brex users?

* Collect your Brex assets like users, locations, departments, and companies in a single asset directory.
* Query your resources using SQL or free text search.
* Automate your security and compliance checks with managed or custom rules.
* Receive notifications when there is a rule change.
* Keep track of resource and configuration changes.

### How does the integration work?

Resmo uses API to do the initial polling and collect existing resources. Following the initial polling, it receives updates and changes in real-time through webhook and regular polling.

#### Available resources

{% embed url="https://docs.resmo.com/resources/brex" %}

## Integration walkthrough

### How to install

1. Sign up or sign in to your Resmo account.
2. Go to your Integrations page and click the Add Integration button.

<figure><img src="../.gitbook/assets/add-new-integration.png" alt=""><figcaption></figcaption></figure>

3\. Add Brex.

<figure><img src="../.gitbook/assets/add-brex.png" alt=""><figcaption></figcaption></figure>

4\. Name your Brex integrations and optionally write a description.

<figure><img src="../.gitbook/assets/brex-integration.png" alt=""><figcaption></figcaption></figure>

5\. Go to **Create Token** under the **Developer -> Settings** page.

<figure><img src="../.gitbook/assets/brex-api-token.jpg" alt=""><figcaption></figcaption></figure>

6\. Create and copy the Read-only Auth Token from your Brex account. Required scopes:

{% hint style="info" %}
* Users Read
* Locations Read
* Departments Read
* Companies Read
{% endhint %}

<figure><img src="../.gitbook/assets/token-scopes.png" alt=""><figcaption></figcaption></figure>

7\. Paste it to the API Token field on the setup page.

<figure><img src="../.gitbook/assets/API.png" alt=""><figcaption></figcaption></figure>

8\. Hit the Create button.

9\. That's it! Now you can start querying your Brex resources.

### How to uninstall

1. Log in to your Resmo account and navigate to the Integrations page.
2. Click the Brex integration you wish to remove.
3. To temporarily pause your Brex integration, click the Disable button. You can also permanently uninstall it by clicking the Delete button.&#x20;

<figure><img src="../.gitbook/assets/disable-delete-integration.png" alt=""><figcaption></figcaption></figure>

### Support

Still have questions? Feel free to contact us via live chat or email us at contact@resmo.com.

