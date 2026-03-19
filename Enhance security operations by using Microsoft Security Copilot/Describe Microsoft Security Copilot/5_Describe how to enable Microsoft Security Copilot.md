# Describe How to Enable Microsoft Security Copilot

To start using Microsoft Security Copilot, organizations need to take steps to onboard the service and users. These include:

- Provision Copilot capacity
- Set up the default environment
- Assign role permissions

---

## Provision Capacity

Security Copilot operates on a provisioned capacity and an overage model. Provisioned capacity is billed by the hour while the overage capacity is billed on usage.

You can flexibly provision Security Compute Units (SCUs) to accommodate regular workloads and adjust them anytime without long-term commitments. An SCU is the unit of measure of computing power used to run Copilot in both the standalone and embedded experiences.

To manage unexpected demand spikes, you can allocate an overage amount to ensure that additional SCUs are available when initially provisioned units are depleted during unexpected workload spikes. Overage units are billed on-demand and can be set as unlimited or a maximum amount. This approach enables predictable billing while providing the flexibility to handle both regular and unexpected usage. See the summary and resources section of this module for links to information on Managing security compute unit usage and Security Copilot pricing.

Before users can start using Copilot, admins need to provision and allocate capacity. To provision capacity:

- You must have an Azure subscription.
- You need to be an Azure owner or Azure contributor, at a resource group level, as a minimum.

Keep in mind that a global Microsoft Entra administrator role doesn't necessarily have the Azure owner or Azure contributor role by default. Microsoft Entra role assignments don't grant access to Azure resources. As a global Microsoft Entra administrator, you can enable access management for Azure resources through the Azure portal. For details, see Elevate access to manage all Azure subscriptions and management groups. Once you've enabled access management to Azure resources, you can configure the appropriate Azure role.

There are two options for provisioning capacity:

- **Provision capacity within Security Copilot (recommended)** - When you first open Security Copilot as an admin, a wizard guides you through the steps in setting up capacity. The wizard prompts you for information including your Azure subscription, resource group, region, capacity name, and the quantity of SCUs.
- **Provision capacity through Azure** - The Azure portal now includes Security Copilot as a service. Selecting the service, opens the page where you input information including your Azure subscription, resource group, region, capacity name, and the quantity of SCUs.

> Note: Regardless of the method you choose, you'll need to purchase a minimum of 1 and a maximum of 100 SCUs.

> Provision through Copilot
<img width="630" height="525" alt="image" src="https://github.com/user-attachments/assets/fd65a671-bf4a-4fe8-aba0-da255544d730" />

> Provision through Azure portal
<img width="630" height="525" alt="image" src="https://github.com/user-attachments/assets/3ab8fa9c-dec3-4456-a78f-8a78bb19e0f6" />

Regardless of the approach you choose to provision capacity, the process takes the information and establishes a resource group for the Microsoft Security Copilot service, within your Azure subscription. The SCUs are an Azure resource within that resource group. Deployment of the Azure resource can take a few minutes.

Once admins complete the steps to onboard to Copilot, they can manage capacity by increasing or decreasing provisioned SCUs within the Azure portal or the Microsoft Security Copilot product itself.

Security Copilot provides a usage monitoring dashboard for capacity owners allowing them to track usage over time and make informed decisions about capacity provisioning. The usage monitoring dashboard provides visibility, for a selected workspace, into the number of units used, the specific plugins employed during sessions, and the initiators of those sessions. The dashboard also allows you to apply filters and export usage data seamlessly. The dashboard includes up to 90 days of data.

<img width="630" height="525" alt="image" src="https://github.com/user-attachments/assets/0886635b-b912-4407-a45e-c32508086809" />

---

## Set Up the Default Environment

To set up the default environment, you need to have, at least, a Security Administrator role.

During the setup of Security Copilot, you're prompted to configure settings. These include:

### SCU Capacity

Select the capacity of SCUs previously provisioned. Each workspace must have its own capacity.

### Data Storage

When an organization onboards to Copilot, one of the available settings determines where your customer data will be stored. Configuration of the data storage location applies at a workspace level. Microsoft Security Copilot operates in the Microsoft Azure data centers in the European Union (EUDB), the United Kingdom, the United States, Australia and New Zealand, Japan, Canada, and South America.

Decide where your prompts are evaluated - You can restrict the evaluation within your geo or allow evaluation anywhere in the world.

### Logging Audit Data in Microsoft Purview

As part of the initial setup and listed under Owner settings in the standalone experience, you can choose to allow Microsoft Purview to process and store admin actions, user actions, and Copilot responses. This includes data from any Microsoft and non-Microsoft Integrations. If you opt in and you already use Microsoft Purview, no further action is needed. If you opt in but aren't already using Purview, you need to follow the Microsoft Purview guides to set up a limited experience. This configuration applies to all workspaces in a tenant.

<img width="630" height="525" alt="image" src="https://github.com/user-attachments/assets/693121d0-60bd-4067-b660-3858f4f80238" />

### Your Organization's Data

The admin must also opt in or opt out of data sharing options. These options are part of the initial setup and also listed under Owner settings in the standalone experience and can be configured per workspace. Turn the toggles on or off for any of the following options:

- **Allow Microsoft to capture data from Security Copilot to validate product performance using human review:** When turned on, customer data is shared with Microsoft for product improvement. Prompts and responses are evaluated to understand whether the right plugins were selected, if the output is what was expected, how responses, latency, and output format can be improved.

- **Allow Microsoft to capture and human review data from Security Copilot to build and validate Microsoft's security AI model:** When turned on, customer data is shared with Microsoft for Copilot AI improvement. Opting in does NOT allow Microsoft to use customer data to train foundational models. Prompts and responses are evaluated to enhance responses and to ensure they're what's expected and useful to you.

For more information about how Microsoft handles your data, see Data security and privacy.

<img width="630" height="525" alt="image" src="https://github.com/user-attachments/assets/d54d7dea-c263-4122-aee8-35455836f9a9" />

### Plugin Settings

The admin manages plugins and configures whether to allow Security Copilot to access data from your Microsoft 365 services. These settings are configured per workspace.

- Configure who can add and manage their own custom plugins and who can add and manage custom plugins for everyone in the organization.
- Manage plugin availability and restrict access. When enabled, admins decide which new and existing plugins will be available to everyone in your organization, and which will be restricted to owners only.
- Allow Security Copilot to access data from your Microsoft 365 services. If this option is turned off, your organization won't be able to use plugins that access Microsoft 365 services. Currently, this option is required for use of the Microsoft Purview plugin. Setting and/or changing this setting requires a user with a Copilot owner role or a global Microsoft Entra administrator role.

<img width="630" height="525" alt="image" src="https://github.com/user-attachments/assets/7aa566e9-cfcf-483d-a664-9a147b1aa419" />

---

## Role Permissions

To ensure that the users can access the features of Copilot, they need to have the appropriate role permissions. Role permissions are configured per workspace.

Permissions can be assigned using Microsoft Entra ID roles or Security Copilot roles. As a best practice, provide the least privileged role applicable for each user.

### Microsoft Entra ID Roles

- Global administrator
- Security administrator
- Security operator
- Security reader

Although these Microsoft Entra ID roles grant users varying levels of access to Copilot, the scope of these roles extends beyond Copilot. For this reason, Security Copilot introduces two roles that function like access groups but aren't Microsoft Entra ID roles. Instead, they only control access to the capabilities of the Security Copilot platform.

### Microsoft Security Copilot Roles

- Copilot owner
- Copilot contributor

The Security Administrator and Global Administrator roles in Microsoft Entra automatically inherit Copilot owner access.

<img width="630" height="525" alt="image" src="https://github.com/user-attachments/assets/ad058309-3eb5-4440-8f09-d1ff08c22b6a" />

Only users that have the global administrator, security administrator, or Copilot owner roles can make role assignments in Copilot by adding/removing members from the Owner and Contributor roles.

A group that admins/owners can include as a member of the Contributor role is the **Recommended Microsoft Security roles group**. This group exists only in Security Copilot and is a bundle of existing Microsoft Entra roles. When you add this group as a member of the Contributor role, all users that are members of the Entra ID roles that are included in the recommended Microsoft Security roles group get access to the Copilot platform. This option provides a quick, secure way to give users in your organization, who already have access to security data used by Copilot through a Microsoft plugin, access to the Copilot platform.

For a detailed listing of the permissions granted for each of these roles, refer to the Assign roles section in Understand authentication in Microsoft Security Copilot.

---

## Copilot Plugins and Role Requirements

Your role controls what activities you have access to, such as configuring settings, assigning permissions, or performing tasks. Copilot doesn't go beyond the access you have. Additionally, individual Microsoft plugins may have their own role requirements for accessing the service and data it represents.

As an example, an analyst that has been assigned a security operator role or a Copilot workspace contributor role is able to access the Copilot portal and create sessions, but to utilize the Microsoft Sentinel plugin would need an appropriate role like Microsoft Sentinel Reader to access incidents in the workspace. To access the devices, privileges, and policies available through the Microsoft Intune plugin, that same analyst would need another service-specific role like the Intune Endpoint Security Manager role.

Generally speaking, Microsoft plugins in Copilot use the OBO (on behalf of) model – meaning that Copilot knows that a customer has licenses to specific products and is automatically signed into those products. Copilot can then access the specific products when the plugin is enabled and, where applicable, parameters are configured. Some Microsoft plugins that require setup may include configurable parameters that are used for authentication in-lieu of the OBO model.

Enabling of individual plugins and configuration of plugins is done per workspace.

---

## Use Cases and Solutions

### Capacity Provisioning Use Cases

- **Handling workload volatility** - Security operations experience unpredictable spikes during major incidents or threat campaigns
  - *Solution:* Provision flexible SCUs with overage allocation (unlimited or capped) to accommodate unexpected demand spikes without service interruption, while maintaining predictable base billing
  - *Reference:* [Manage Security Compute Units in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot/security/manage-usage)

- **Azure administrator access gaps** - Global Microsoft Entra administrators lack necessary Azure roles to provision Copilot capacity
  - *Solution:* Elevate access through the Azure portal to manage all Azure subscriptions and management groups, then configure appropriate Azure owner or contributor roles at the resource group level
  - *Reference:* [Elevate Access for Azure Administrators](https://learn.microsoft.com/en-us/azure/role-based-access-control/elevate-access-global-admin)

- **Capacity optimization decisions** - Admins need visibility into actual usage patterns to right-size SCU allocation
  - *Solution:* Use the usage monitoring dashboard to track SCU consumption, plugin usage, and session initiators over 90 days, applying filters and exporting data to inform capacity adjustments
  - *Reference:* [Microsoft Security Copilot Usage Monitoring](https://learn.microsoft.com/en-us/copilot/security/manage-usage#monitor-usage)

### Environment Configuration Use Cases

- **Data residency compliance** - Organizations must store Copilot data in specific geographic regions per regulatory requirements
  - *Solution:* Configure data storage location at workspace level during setup, selecting from available Azure data centers (EUDB, UK, US, Australia/NZ, Japan, Canada, South America)
  - *Reference:* [Microsoft Security Copilot Data Storage](https://learn.microsoft.com/en-us/copilot-security/privacy-data-security)

- **Audit trail requirements** - Security teams need comprehensive logging of admin actions, user activities, and Copilot responses
  - *Solution:* Opt in to Microsoft Purview audit logging during initial setup to process and store all administrative and user actions across Microsoft and non-Microsoft integrations
  - *Reference:* [Microsoft Purview Audit Logging](https://learn.microsoft.com/en-us/purview/audit-logging)

- **Balancing product improvement with data privacy** - Organizations want to contribute to Copilot improvement without compromising sensitive data
  - *Solution:* Selectively enable data sharing toggles per workspace—opt in to "validate product performance" for operational metrics, or "build AI models" for response quality improvement, with assurance that customer data is never used to train foundational models
  - *Reference:* [Microsoft Security Copilot Data Privacy](https://learn.microsoft.com/en-us/copilot-security/privacy-data-security)

- **Controlled plugin ecosystem** - Organizations need to manage which plugins are available to users and who can configure them
  - *Solution:* Configure plugin settings per workspace to restrict custom plugin management to specific users, manage plugin availability (organization-wide vs. owners-only), and control Microsoft 365 data access (required for Microsoft Purview plugin)
  - *Reference:* [Manage Plugins in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/manage-plugins)

### Role Assignment Use Cases

- **Principle of least privilege** - Organizations need to grant Copilot access without over-permissioning users
  - *Solution:* Assign Security Copilot-specific roles (Copilot owner, Copilot contributor) that function only within the Copilot platform, rather than broader Microsoft Entra ID roles, following best practice of least privileged access
  - *Reference:* [Assign Roles in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/assign-roles)

- **Rapid team onboarding** - Security teams already have Microsoft security product access and need quick Copilot provisioning
  - *Solution:* Add the "Recommended Microsoft Security roles group" as a member of the Contributor role to automatically grant Copilot access to all users who already have security data access through Microsoft plugins
  - *Reference:* [Microsoft Security Copilot Role Groups](https://learn.microsoft.com/en-us/copilot-security/assign-roles#recommended-microsoft-security-roles-group)

- **Cross-product security analysis** - Analysts need to use Copilot with multiple Microsoft security products
  - *Solution:* Ensure users have both Copilot workspace access (via Security Operator or Copilot Contributor roles) AND service-specific roles for each plugin (e.g., Microsoft Sentinel Reader for Sentinel incidents, Intune Endpoint Security Manager for Intune data), as Copilot respects existing product permissions under the OBO model
  - *Reference:* [Understand Authentication in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/understand-authentication)

- **Plugin authentication exceptions** - Certain Microsoft plugins require explicit authentication rather than automatic OBO sign-in
  - *Solution:* For plugins requiring setup, configure authentication parameters during workspace-level plugin enablement, using configurable parameters in lieu of the standard OBO model
  - *Reference:* [Configure Plugins in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/manage-plugins#configure-plugins)

---

## References

- [Microsoft Security Copilot Documentation](https://learn.microsoft.com/en-us/copilot/security/)
- [Provision Capacity for Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/provision-capacity)
- [Manage Security Compute Unit Usage](https://learn.microsoft.com/en-us/copilot-security/manage-usage)
- [Microsoft Security Copilot Pricing](https://azure.microsoft.com/en-us/pricing/details/security-copilot/)
- [Elevate Access to Manage Azure Subscriptions](https://learn.microsoft.com/en-us/azure/role-based-access-control/elevate-access-global-admin)
- [Assign Roles in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/assign-roles)
- [Understand Authentication in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/understand-authentication)
- [Manage Plugins in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/manage-plugins)
- [Microsoft Security Copilot Data Privacy and Security](https://learn.microsoft.com/en-us/copilot-security/privacy-data-security)
- [Microsoft Purview Audit Logging](https://learn.microsoft.com/en-us/purview/audit-logging)
