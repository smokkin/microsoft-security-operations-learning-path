# Describe Workspaces

Copilot workspaces are separate work environments within the tenant in which your Copilot instance is operating.

To help you better understand the concept of workspaces, we use the analogy of house with multiple rooms. Each room is configured to be optimized for its function and the people that use that room. When someone enters the house, they might have access to some rooms but not others.

You can think of Copilot Workspaces fitting into this analogy. A Copilot workspace is analogous to a room in a house. You can also think of the house as analogous to a tenant. In the same way that a house has multiple rooms, the tenant in which Copilot is operating can have multiple workspaces.

Through the tenant-switching capability in Security Copilot, a user can select in which tenant they'll be working. In our analogy, this is a Copilot user getting access to the house. Once the tenant is selected, a Copilot user can access and work in any workspace (room in the house) to which they have access, within the context of their role permissions in that workspace.

---

## Benefits of Copilot Workspaces

There are many benefits to Copilot workspaces.

- Set up individual workspaces to address specific team needs.
- Manage and map costs based on team needs and budgets.
- Ensure critical workflows aren't disrupted by throttling.
- Store session data according to geo-specific regulations.
- Set up and manage specific plugins, promptbooks, and files for specific team needs.
- Experiment with custom plugins and promptbooks before organization-wide deployment.

---

## Create a Workspace

You need to be at least a Security Administrator to create new workspaces for your organization. A workspace is powered by a capacity resource (SCUs). To attach capacity to a workspace, you also need to be an Azure subscription owner or contributor.

There are several entry points for you to create a new workspace:

- From the landing page of the Security Copilot portal
- From the Manage workspaces section of the Owner settings page
- From the breadcrumb

> From the breadcrumb
<img width="396" height="322" alt="image" src="https://github.com/user-attachments/assets/1067fde6-0ccd-4af9-9e13-7c25bb7cabce" />

> Owner settings page
<img width="1576" height="696" alt="image" src="https://github.com/user-attachments/assets/eb81c802-bb09-46ce-abd5-94ec5549764f" />

From any of entry points, select **New Workspace**.

To Set up the workspace, specify a name for the workspace, create or select an existing capacity, select the data storage location, and define your data sharing preferences. These choices are all specific to this workspace and can be different from the selections made at the time Security Copilot was initially set up (the first run experience).

Confirm that you acknowledge and agree to the terms and conditions, then select **Create**.

> Create a workspace
<img width="665" height="659" alt="image" src="https://github.com/user-attachments/assets/107df238-a84b-4c64-91ea-9e9dc04c46e5" />

> Create capacity
<img width="677" height="777" alt="image" src="https://github.com/user-attachments/assets/f942cf9a-b9ab-408b-96e3-6799ac96095a" />

---

## Configure Workspaces

Once the workspace is created and selected, it can be configured with unique settings and permissions, allowing you to tailor the environment to meet the specific needs of your team. This includes assigning roles, managing access, and setting up plugins and promptbooks that are relevant to the workspace.

Decisions and configuration made in plugin settings and role permissions apply specifically to the workspace in which they're being configured.

Decisions and configurations within "owner settings" apply specifically to the workspace that's being configured, with one exception: Audit Logging enablement can only be changed by Security Admins and applies to all workspaces.

<img width="733" height="712" alt="image" src="https://github.com/user-attachments/assets/08b24594-9e52-45d4-83a5-84d3363e0e1e" />

---

## Manage Workspaces

Owners can view, navigate between, manage capacity allocations, and delete workspaces that they own from the Manage Workspaces page.

> Manage workspaces
<img width="1685" height="508" alt="image" src="https://github.com/user-attachments/assets/5e4273bf-fcd0-457d-92bc-0523e120e625" />

> Assign and switch capacity
<img width="1685" height="538" alt="image" src="https://github.com/user-attachments/assets/9c5ee356-8ba2-46d9-b165-c9926aae5910" />

---

## Use Workspaces

From the main landing page, users can select the current workspace, which opens the drop-down menu where users can select available workspaces to which they have access. They can also set their preferred workspace in cases where they have access to multiple workspaces. Owners are also given the option to manage workspaces, manage capacity usage, and create a new workspace.

Once in a workspace, users can start using promptbooks, enter prompts directly in the prompt bar, and all the features of Copilot for which they have permissions.

> Note: If users have been doing work with Copilot in one of the Security product portals (for example Defender, Intune, Microsoft Entra, or Purview) and they switch their preferred workspace, they need to reload or sign out & sign in to the portals to continue working with Copilot in those portals. If they don't, they'll encounter an error.

> Workspace
<img width="682" height="507" alt="image" src="https://github.com/user-attachments/assets/1e33e76a-61d4-4876-8c3a-52757cd4e794" />

> Workspace menu option
<img width="682" height="507" alt="image" src="https://github.com/user-attachments/assets/f320b486-fe2e-4828-b39d-b45f9ad9164f" />

---

## Use Cases and Solutions

### Workspace Creation Use Cases

- **Team-specific environment setup** - Different security teams (SOC, threat intel, compliance) need isolated environments with tailored configurations
  - *Solution:* Create dedicated workspaces via the Security Copilot portal landing page, Owner settings, or breadcrumb navigation, specifying unique names, SCU capacity, data storage locations, and data sharing preferences per team
  - *Reference:* [Create a Workspace in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot/security/manage-workspaces)

- **Controlled capacity allocation** - Organizations need to allocate compute resources to specific departments with budget accountability
  - *Solution:* As a Security Administrator with Azure subscription owner/contributor rights, create workspaces with dedicated SCU capacity attachments, enabling cost mapping to specific teams

### Workspace Configuration Use Cases

- **Role-based access control per team** - Teams require different permission levels within their respective environments
  - *Solution:* Configure unique role assignments and plugin settings per workspace, ensuring decisions apply specifically to that workspace without affecting others

- **Pre-production testing environment** - Security teams need to validate custom plugins and promptbooks before production deployment
  - *Solution:* Create isolated workspaces for experimentation with specific plugins, promptbooks, and files, allowing testing without impacting organization-wide configurations

- **Data residency compliance** - Multi-national organizations must store session data in specific geographic regions per regulatory requirements
  - *Solution:* Select geo-specific data storage locations during workspace setup (EU, UK, US, Australia/NZ, Japan, Canada, South America) to adhere to local regulations

### Workspace Management Use Cases

- **Capacity reallocation during incidents** - Critical security events require temporary compute resource increases
  - *Solution:* Owners navigate to Manage Workspaces to reassign capacity allocations between workspaces, ensuring critical workflows aren't disrupted by throttling

- **Workspace lifecycle management** - Decommissioned teams or projects require cleanup of unused environments
  - *Solution:* Owners view, navigate between, and delete workspaces they own from the Manage Workspaces page

### Multi-Workspace Usage Use Cases

- **Cross-functional security operations** - Analysts support multiple teams with different workspace access needs
  - *Solution:* Users select from the workspace drop-down menu on the main landing page to switch between accessible workspaces, setting preferred defaults for quick access

- **Embedded experience synchronization** - Users encounter errors when switching workspaces while using Copilot in Microsoft security portals
  - *Solution:* After switching preferred workspaces, reload the page or sign out and sign in to Defender, Intune, Microsoft Entra, or Purview portals to continue working with Copilot in those embedded experiences

### Audit and Compliance Use Cases

- **Organization-wide audit policy** - Compliance requires consistent audit logging across all security operations
  - *Solution:* Security Admins enable Audit Logging in owner settings, noting this configuration applies to all workspaces unlike other workspace-specific settings

---

## References

- [Microsoft Security Copilot Workspaces Overview](https://learn.microsoft.com/en-us/copilot-security/workspaces)
- [Create a Workspace in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/create-workspace)
- [Configure Workspace Settings](https://learn.microsoft.com/en-us/copilot-security/configure-workspace)
- [Manage Workspaces](https://learn.microsoft.com/en-us/copilot-security/manage-workspaces)
- [Microsoft Security Copilot Roles and Permissions](https://learn.microsoft.com/en-us/copilot-security/assign-roles)
- [Data Storage and Residency](https://learn.microsoft.com/en-us/copilot-security/privacy-data-security)
- [Audit Logging in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/audit-logging)
