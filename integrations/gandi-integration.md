---
description: Guide for Resmo Gandi Integration.
---

# Gandi Integration

## Resmo + Gandi Integration Fundamentals

![](../.gitbook/assets/gandi-logo.png)

Resmo integrates with Gandi to enhance the security and compliance of your Gandi environment.

### What does Resmo offer to Gandi users?

* Consolidate and monitor all your Gandi resources in one place.
* Query your Gandi organizations, domains, certificates, and more.
* Set up rules to continuously assess your Gandi resources.
* Set up notification rules to get alerted on rule violations.

### How does the integration work?

Once you sign up to Resmo, you can easily integrate your account with Gandi using an API key. Resmo uses API to do the initial polling and collect existing resources. Then, we receive resource changes and updates in real-time by regular polling.

[Available Resources](https://docs.resmo.com/resources/gandi)

### Common queries and rules

* List DNSSEC enabled domains
* Detect live DNS supported domains
* List domain registries that end in a month
* Find domain redirection counts per type
* Find changed domain automatic renewal statuses
* See certificates with valid status

### Integration Walkthrough

#### **How to Install**

1. Log in to your Resmo account and go to Settings>Integrations. Then, select Gandi.
2. Click the Add Integration button at the bottom right corner of the opening modal.

3\. Go to your Gandi account and create an API token from your User Settings -> Login and Security Options -> Password & Access Restrictions tab if you have not created it already.

![](../.gitbook/assets/gandi-user-settings.png)

* Resmo needs **View Organization**, **See and renew domain names** and **See & download SSL certificates** permissions to collect your data. As a best practice, you can create a member under the team with that permissions and use the API key of the member in Resmo.

![](../.gitbook/assets/gandi-security.png)

4\. Enter the API key on the integration screen’s API key field.

5\. Hit the create button, and you are ready to run queries.

#### **How to Uninstall**

There are two options:

* To temporarily pause your Gandi integration, click the Disable button.
* To permanently uninstall it, click the Delete button.

Go to Integrations -> Gandi.

Navigate to the Connected Integrations tab on the opening modal.

Click the integration you want to remove, then either the Disable or Delete button based on your choice.

### Support

For further questions or information, please get in touch with us via live chat or at contact@resmo.com.
