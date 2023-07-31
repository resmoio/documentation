---
description: Guide for Resmo Vercel integration
---

# Vercel Integration

## Resmo + Vercel Integration Fundamentals

<figure><img src="../.gitbook/assets/vercel-logo.png" alt=""><figcaption></figcaption></figure>

Resmo integrates with Vercel to provide asset visibility, security, and compliance for your environment.

### What does Resmo offer to Vercel users?

* Collect your directory assets like members, teams, and projects from your Vercel account.
* Query your Vercel members, teams, projects, and more using SQL or free text search.
* Set up security rules to continuously evaluate your resource security.
* Understand resource relationships in context with graph maps.

### How does the integration work?

Resmo uses API to do the initial polling and collect existing resources. Following the initial polling, it receives updates and changes in real-time through webhook and regular polling.

#### Available resources

Resources you can collect with your Resmo Vercel integration include domains, checks, members, projects, and more.

**See the complete list:**

{% embed url="https://resources.resmo.com/vercel" %}

## Integration walkthrough

### How to install

1. Select Vercel on the Intagrations page.
2. Click the Add Integration button at the bottom right corner of the opening modal.
3. Log in to your Vercel account on a new tab.
4. Go to the [Tokens Page](https://vercel.com/account/tokens) on your Vercel account. This page can be found by clicking your avatar and then clicking on Settings.

<figure><img src="../.gitbook/assets/account-settings.png" alt=""><figcaption></figcaption></figure>

5\. Click Create and select the full access scope.

<figure><img src="../.gitbook/assets/access-scope.png" alt=""><figcaption></figcaption></figure>

6\. Select the desired expiration time for your token.

<figure><img src="../.gitbook/assets/expiration-date-for-vercel-api.png" alt=""><figcaption></figcaption></figure>

7\. Click "Create Token".

<figure><img src="../.gitbook/assets/vercel-api-token-generation.png" alt=""><figcaption></figcaption></figure>

8\. Copy your token.

9\. Paste it to the Token field on the setup page.

<figure><img src="../.gitbook/assets/paste-token.png" alt=""><figcaption></figcaption></figure>

10\. Hit the Create button.

11\. All set! Now you can start running queries on your Vercel resources.

### How to uninstall

1. Select Vercel on your Integrations page.
2. Navigate to the Connected Integrations tab on the opening modal.
3. Click the Vercel integration you want to uninstall.
4. To temporarily pause the integration, click the Disable button. This way, you'll be able to enable it back later. To permanently uninstall it, click the Delete button. This action cannot be undone.

<figure><img src="../.gitbook/assets/delete-disable-buttons (1).png" alt=""><figcaption></figcaption></figure>
