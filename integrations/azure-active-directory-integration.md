---
description: Integration guide for Resmo Azure Active Directory Integration.
---

# Azure Active Directory Integration

## Resmo + Azure Active Directory Integration Fundamentals

![](../.gitbook/assets/azuread-logo.png)

Resmo easily integrates with AzureAD to secure and query your entire resource asset.

### What does Resmo offer to AzureAD users?

* Collect and monitor all AzureAD resources in near real-time from one place
* Query your assets with the simplified SQL language
* Run automated rule checks with managed or custom rules
* Get notified of rule changes in real-time
* Discover historic data for your resource changes, queries, and rule violations

### How does the integration work?

Resmo connects with AzureAD through an OAuth flow. Then, it initiates polling and aggregating your existing resources. After the initial polling, Resmo performs polling at regular intervals to collect resource changes in real-time.

{% embed url="https://docs.resmo.com/resources/azuread" %}

{% hint style="info" %}
**Tip:** Use [Audit Logs](../audit-logs/audit-logs.md) for comprehensive monitoring of all Azure Active Directory activities and system events.
{% endhint %}

### Common queries and rules

* View AzureAD organization verified domains.
* List guest users.
* See Service Principal OAuth2 permissions.
* Find user groups that are not assignable to any role.
* List user accounts that are not enabled.

### Integration walkthrough

#### How to Install

1. Sign up or sign in to Resmo.
2. Navigate to Integrations and select Azure Active Directory.
3. Click the Add Integration button from the bottom right corner of the opening modal.
4. Click Create.
5. You'll be redirected to Azure. Accept permissions.
6. Your integration is ready! Now you can start querying your Azure Active Directory resources!

#### How to Uninstall

1. Log in to your Resmo account.
2. Go to your Integrations page and select Azure AD.
3. Go to the Connected Integrations tab from the opening modal and select the one you want to remove or disable.

![](../.gitbook/assets/azuread-integration-delete.png)

4\. To temporarily pause the integration, click the Disable button from the top right. Or, you can permanently remove it by clicking the Delete button.

5\. Optionally, you can remove your oAuth token after uninstalling the integration permanently. Follow instructions [here](https://docs.microsoft.com/en-us/azure/active-directory/enterprise-users/users-revoke-access#azure-active-directory-environment).

### Support

If you have any questions about the Azure Active Directory integration or Resmo in general, feel free to email us at contact@resmo.com or contact us via live chat on our website.
