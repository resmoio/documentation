---
description: Guide for Resmo LastPass integration
---

# LastPass Integration

## Resmo + LastPass Integration Fundamentals

<figure><img src="../.gitbook/assets/lastpass-logo.png" alt=""><figcaption></figcaption></figure>

Resmo integrates with LastPass to help you safeguard your LastPass assets with complete visibility, security, and compliance.

### What does Resmo offer to LastPass users?

* Collect your LastPass directory assets like users and groups.
* Query your LastPass resources using SQL or free text search.
* Set up custom rules and run custom SQL queries to improve asset visibility.
* Get notified of critical rule changes in real-time.

### How does the integration work?

Resmo uses API to do the initial polling and collect existing resources. Following the initial polling, it receives updates and changes in real-time through webhook and regular polling.

#### Available resources

{% embed url="https://docs.resmo.com/resources/lastpass" %}

## Integration walkthrough

### How to install

1. Sign up or sign in to Resmo. Then, go to your Integrations page.
2. Click the Add Integration button and add LastPass.

<figure><img src="../.gitbook/assets/add-lastpass.png" alt=""><figcaption></figcaption></figure>

3\. Type a descriptive name for your LastPass integration and optionally a description.

<figure><img src="../.gitbook/assets/lastpass-resmo.png" alt=""><figcaption></figcaption></figure>

4\. Go to the Admin Dashboard of your LastPass account.

5\. Copy your account number under the dashboard header.

6\. Paste it to the Customer Id field on the setup page.

<figure><img src="../.gitbook/assets/lastpass-integration.png" alt=""><figcaption></figcaption></figure>

7\. Go to the Advanced page on your LastPass account.

8\. Go to the Enterprise API section.

9\. Create a Provisioning Hash, or if you already have one, copy it.

<figure><img src="../.gitbook/assets/create-hash.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/copy-paste-the-key.png" alt=""><figcaption></figcaption></figure>

10\. Paste it to the Provisioning Hash field on the integration setup page.

11\. Click the Create button on your Resmo LastPass integration screen.

12\. All set! Now you can start running queries on your LastPass resources.

### How to uninstall

1. Go to your Integrations page on Resmo.
2. Click the LastPass integration you wish to uninstall.
3. To temporarily pause the integration, click the Disable button from the top right. For permanent removal, click the Delete button.

<figure><img src="../.gitbook/assets/lastpass-disable.png" alt=""><figcaption></figcaption></figure>

### Support

Reach out to our team for support and troubleshooting requests via live chat or email us at contact@resmo.com.
