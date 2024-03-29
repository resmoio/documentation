---
description: Guide for Resmo DigitalOcean integration
---

# DigitalOcean Integration

## Resmo + DigitalOcean Integration Fundamentals

<figure><img src="../.gitbook/assets/digitalocean-logo.png" alt=""><figcaption></figcaption></figure>

Resmo integrates with DigitalOcean to make sure your DigitalOcean environment is safe and compliant.

### What does Resmo offer to DigitalOcean users?

* Collect your directory assets, like CDN endpoints, apps, firewalls, certificates, and more, on a single platform.
* Query your DigitalOcean app, domain, domain records, Kubernetes clusters, and more using SQL and free text search.
* Set up automated security rules to evaluate your DigitalOcean asset security posture.
* Get near real-time notifications of security rule violations to avoid vulnerabilities in time.

### How does the integration work?

Resmo uses API to do the initial polling and collect existing resources. Following the initial polling, it receives updates and changes in real-time through regular polling.

#### Available resources

{% embed url="https://resources.resmo.com/digitalocean" %}

## Integration walkthrough

### How to install

1. Select DigitalOcean on the Integrations page of your Resmo account.
2. Click the Add Integration button at the bottom right corner of the opening modal.
3. Hit the Create button.

<figure><img src="../.gitbook/assets/add-digitalocean.png" alt=""><figcaption></figcaption></figure>

4. You'll be redirected to DigitalOcean. Accept permissions.&#x20;
5. You are ready! Now you can start querying your DigitalOcean resources!

### How to uninstall

1. Select DigitalOcean on your Integrations page.
2. Navigate to the Connected Integrations tab on the opening modal.
3. Click the DigitalOcean integration you want to uninstall.
4. To temporarily disable the integration, click the **Disable** button from the top right. You can enable it back later on. For permanent deletion, click the Delete button instead. This action cannot be undone.

<figure><img src="../.gitbook/assets/disable-delete-digitalocean.png" alt=""><figcaption></figcaption></figure>
