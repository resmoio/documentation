---
description: Guide for Resmo Kolide integration
---

# Kolide Integration

## Resmo + Kolide Integration Fundamentals

<figure><img src="../.gitbook/assets/kolide-logo.png" alt=""><figcaption></figcaption></figure>

Resmo's agent-free, one-click integration with Kolide provides centralized visibility, security, and compliance for your Kolide asset environment.

### What does Resmo offer to Kolide users?

* Collect your directory assets like devices, users, and checks from your Kolide account.
* Query your Kolide users, teams, roles, and much more.
* Automatically audit your Kolide resources' security and compliance
* Set up rule notifications based on Kolide resource configurations.

### How does the integration work?

Resmo uses API keys created from the Kolide Admin page. Our application uses API to make the initial polling and receive existing resources. Then, we receive resource changes and updates in real-time by regular polling.

#### Available resources

Resmo consolidates Kolide resources in one place, including devices, identities, checks, and more.

{% embed url="https://docs.resmo.com/resources/kolide" %}

## Integration Walkthrough

### How to install

1. Go to your Integrations page and select Kolide.
2. Click the Add Integration button at the bottom right corner of the opening modal.
3. Open a new tab on your browser and go to your Kolide account.
4. Create an API Key from Kolide [Settings Page](https://k2.kolide.com/x/settings/admin/api). Then, copy it.
5. Fill the form with your copied Kolide API Key and click Create.
6. You are now ready! Now you can start querying your Kolide resources!

### How to uninstall

1. Go to Integrations -> Kolide.
2. From the Connected Integrations tab on the opening modal, select the Kolide integration you wish to remove.
3. You can temporarily disable or permanently delete your integration from the top right buttons (Disable - Delete.)&#x20;

<figure><img src="../.gitbook/assets/kolide-config.png" alt=""><figcaption></figcaption></figure>

### Support

If you still have any questions about your Resmo Kolide integration, contact us via live chat or email us at contact@resmo.com.
