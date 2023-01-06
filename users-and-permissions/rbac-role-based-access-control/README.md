---
description: This feature is only available in the enterprise plan.
---

# RBAC (Role-Based Access Control)

**Role-Based Access Control** restricts access to specific resources based on a person's defined role within an organization. Through RBAC, you can control what each role can do at a granular or broad level. Individuals can only access and see information, such as integrations or resources necessary to perform their job. &#x20;

**The RBAC management** feature provides policies and roles to manage access controls. Policies are access/deny statements that can be attached to roles to define their permissions. This ensures that an individual is granted only necessary permissions and can't access sensitive data beyond their access level or perform higher-level tasks.

{% hint style="info" %}
There are two types of [roles on Resmo](https://docs.resmo.com/product/users-and-permissions/rbac-role-based-access/custom-roles-and-policies#roles).

* **Managed roles:** Created by default and managed by Resmo. They cannot be edited or deleted.
* **Custom roles:** Can be created, edited, and deleted by users.

Also, [see available user roles](../user-roles.md).
{% endhint %}

### [Roles](https://docs.resmo.com/product/users-and-permissions/rbac-role-based-access/custom-roles-and-policies#roles)

* Users can list all roles from Settings>Roles and see details of each. Custom roles can be created, edited, and deleted. [See how to create a custom role](https://docs.resmo.com/product/users-and-permissions/rbac-role-based-access/custom-roles-and-policies#how-to-create-a-custom-role).
  * A role can have a maximum of 10 policies.
  * Existing users in an account can be updated with existing roles.&#x20;
  * A user can invite users with existing Roles from the User Invitation page. By default, an invited user has UserRole.

### [Policies](https://docs.resmo.com/product/users-and-permissions/rbac-role-based-access/custom-roles-and-policies#policies)

* Policies can be listed from Settings>Policies. Each policy can be seen in detail, while custom policies can also be edited. Policies comprise role a name, description, and statement. [See how to create a custom policy](https://docs.resmo.com/product/users-and-permissions/rbac-role-based-access/custom-roles-and-policies#how-to-create-a-custom-policy).
* [Statements](https://docs.resmo.com/product/users-and-permissions/rbac-role-based-access/custom-roles-and-policies#statements) comprise effect, service, action, and type.
  * Users can leverage the UI dropdown to manage statements or activate the Advanced Mode to use JSON mode when creating a policy.
  * Changes made through the UI dropdown can be seen in JSON mode or vice versa.
  * A user can create a maximum of 10 statements inside a policy.
