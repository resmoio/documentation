---
description: Guide for Resmo JumpCloud integration
---

# JumpCloud Integration

## Resmo + JumpCloud Integration Fundamentals

<figure><img src="../.gitbook/assets/jumpcloud-logo (1).png" alt=""><figcaption></figcaption></figure>

Resmo integrates with JumpCloud to help you keep your JumpCloud assets and configurations like users, devices, policies, and groups secure and compliant.

### What does Resmo offer to JumpCloud users?

* Collect your directory assets like devices, users, groups, and policies from your JumpCloud account.
* Query your JumpCloud devices, users, groups, policies, resource changes, and more.
* Run automated security rules to evaluate your JumpCloud assets and configurations against security best practices
* Receive timely notifications based on JumpCloud resource configurations and changes.

### How does the integration work?

Resmo uses an API key created from your JumpCloud Admin page. Our application uses API to make the initial polling and receive existing resources. Then, we receive resource changes and updates in real-time through regular polling.

**Available resources**

Available resources you can collect with Remso include directories, applications, users, policies, devices, and more.

See the complete list:

{% embed url="https://docs.resmo.com/resources/jumpcloud" %}

{% hint style="info" %}
**Tip:** Use [Audit Logs](../audit-logs/audit-logs.md) for comprehensive monitoring of all JumpCloud activities and system events.
{% endhint %}

## Integration walkthrough

### How to install

1. Select JumpCloud on the Integrations page on your Resmo account.
2. Click the Add Integration button at the bottom right corner of the opening modal.
3. Log in to your JumpCloud account on a new tab on your browser.
4. Create a read-only admin user via **Settings** -> **Administrators** -> **Create a new administrator.**

{% hint style="info" %}
The Role should be 'Read Only' and select Multi-factor Authentication also for best practices!
{% endhint %}

<figure><img src="../.gitbook/assets/administrators.png" alt=""><figcaption></figcaption></figure>

4. Login new created user and copy the user's API Key '**My API Key**' section, which can be accessible by clicking the User Icon from the top right of the page.

<figure><img src="../.gitbook/assets/create-api-key (1).png" alt=""><figcaption></figcaption></figure>

5. Return to your Resmo JumpCloud integration page and paste the API Key in the related field. Then, click Save.

<figure><img src="../.gitbook/assets/enter-api-key.png" alt=""><figcaption></figcaption></figure>

6. You are now ready! Now you can start querying your JumpCloud resources!

### How to uninstall

1. Select JumpCloud on your Integrations page.
2. Navigate the Connected Integrations tab on the opening modal and select the JumpCloud integration you wish to uninstall.
3. From there, you have two options. You can choose to temporarily disable it by clicking the Disable button or permanently uninstall it by clicking the Delete button.

<figure><img src="../.gitbook/assets/disable-delete (1) (1).png" alt=""><figcaption></figcaption></figure>

### Troubleshooting

If you still have questions or issues about the Resmo JumpCloud integration, contact our team via live chat or email us at [contact@resmo.com](mailto:contact@resmo.com).
