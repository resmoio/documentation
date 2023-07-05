---
description: Guide for Resmo Fly.io integration
---

# Upstash Integration

## Resmo + Upstash Integration Fundamentals

<figure><img src="../.gitbook/assets/upstash-logo.png" alt=""><figcaption></figcaption></figure>

Resmo integrates with Upstash in one click to help you keep your Upstash assets continuously secure and compliant.

### What does Resmo offer to Upstash users?

* Create an asset inventory for your Upstash resources, including Redis Databases, Kafka Clusters, users, and more.&#x20;
* Query your resources, configurations, and changes with the flexible SQL engine.
* Assess your resource and configuration security and compliance using rules
* Set up notification rules to get notified of critical changes

### How does the integration work?

Resmo uses API keys created by a user. Ensure that you have Our application uses API to make the initial polling and receive existing resources. Then, we receive resource changes and updates in real-time by regular polling.

#### Available resources

Resmo aggregates Upstash resources in one place, including Kafka topics, Kafka clusters, Redis databases, and more.

{% embed url="https://docs.resmo.com/resources/upstash" %}

## Integration Walkthrough

### How to install

1. Select Upstash on your Integrations page on Resmo.
2. Click the Add Integration button at the bottom right corner of the opening modal.
3. Ensure that the related team or personal account is selected.
4. Open your Upstash account on a new tab on your browser.
5. Create an API Key from Upstash [Settings Page](https://console.upstash.com/account/api).
6. Fill the form with API Key and user email address and click Create.
7. All done! Now you can start querying your Upstash resources!

### How to uninstall

1. Select Flyio on your Integrations page.
2. From the Connected Integrations tab on the opening modal, click the Upstash integration you want to uninstall.
3. To temporarily pause the integration, click the Disable button; to permanently remove it, click the Delete button.&#x20;

<figure><img src="../.gitbook/assets/upstash-config.png" alt=""><figcaption></figcaption></figure>

### Support

For further questions and issues regarding your Resmo Upstash integration, contact us via live chat or email us at contact@resmo.com.&#x20;
