---
description: Guide for Resmo Snyk Integration.
---

# Snyk Integration

## Resmo + Snyk Integration Fundamentals

![](../.gitbook/assets/synk-logo.png)

Resmo integrates with Snyk to ensure your Snyk environment is safe and compliant.

### What does Resmo offer to Snyk users?

* Consolidate and visualize all Snyk resources in one place
* Query your resources like integrations, dependencies, issues, and members
* Continuously assess your assets and configurations for vulnerabilities
* Set up notification rules to get alerted on rule violations
* Utilize conformance packs to run compliance diagnoses across your resources&#x20;

### How does the integration work?

Once you sign up to Resmo, you can easily integrate your account with Snyk using an API key. Resmo uses API to do the initial polling and collect existing resources. Then, we receive resource changes and updates in real-time by regular polling.

{% embed url="https://resources.resmo.com/snyk" %}

### Integration Walkthrough

#### **How to Install**

1. Login to your Resmo account.
2. Navigate to Integrations and select Synk.
3. Click the Add Integration button from the bottom right corner of the opening modal.

4\.  Then, go to your Snyk account and create an API token from your Account Settings -> General -> Auth Token field if you have not created it already.

![](../.gitbook/assets/snyk-auth-token.png)

5\. Now, return to Resmo and enter the API key on the integration screen’s API key field.

![](../.gitbook/assets/snyk-api-key-field.png)

6\. Hit the Create button, and you are ready to run queries.

**How to Uninstall**

1. Go to Settings->Integrations-> Synk.
2. Navigate to the Connected Integrations tab and select the Snyk integration you want to remove. You have two options;

* To temporarily pause the integration, click Disable.
* To permanently uninstall it, click Delete. Note that this action cannot be undone.

### FAQ

* **Does the Synk Resmo integration require a certain Snyk pricing plan?**

The Snyk API is available to customers on [Business and Enterprise plans](https://snyk.io/plans) and allows you to integrate with Snyk.
