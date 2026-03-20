# Describe the Features Available in the Standalone Experience of Microsoft Security Copilot

Microsoft Security Copilot can be accessed through the dedicated site, referred to as the standalone experience. It is through the standalone experience that users access the landing page or portal to the platform. To ensure that the users can access the features of Copilot, they need to have the appropriate role permissions. For more information on role-based access control for Copilot, see the Assign roles section of Understand authentication in Microsoft Security Copilot.

There are some key landmarks on the Copilot landing page (portal) to which the user can navigate.

- Home menu
- Workspaces
- Prompts to try
- Prompt bar

<img width="1312" height="654" alt="image" src="https://github.com/user-attachments/assets/d6c9569d-364d-496e-8073-969e905d15a9" />

---

## Home Menu

The home menu is accessed by selecting the hamburger icon located on the top left corner of the Copilot landing page.

From the home menu, the user can navigate as follows:

<img width="533" height="418" alt="image" src="https://github.com/user-attachments/assets/b8d4db78-b310-41bb-a9ff-ca94ee9ad9a6" />

### Active Agents

Active Agents, which are AI-powered assistants built into Microsoft Security Copilot available for you to choose from. Depending on your role, you can either set them up or access the agent to run it. This page lists Microsoft and non-Microsoft agents that offer significant benefits for security teams and IT operations by automating routine tasks and freeing up valuable time for teams to concentrate on strategic initiatives and complex problem-solving.

<img width="1116" height="454" alt="image" src="https://github.com/user-attachments/assets/6ea32432-2f31-49b7-b90f-785f15457c7d" />

### Promptbooks

Promptbooks, which includes builtin and custom promptbooks. Information about each promptbook is provided, including the description, the number of prompts, the owner, and more. Selecting the Get started button opens the promptbook so you can start using it. You can also select the ellipses for more options.

<img width="1220" height="659" alt="image" src="https://github.com/user-attachments/assets/be22785d-ee60-4894-b67d-c5634f23d5af" />

### Build (Preview)

Build (preview) takes users to the page where You can extend Security Copilot by building custom agents tailored to your organization's specific security and operational needs. Security Copilot empowers developers to build, test, and publish agents to Security Copilot. Additional information on Microsoft Security Copilot agents is covered in the training module Describe Microsoft Security Copilot agents.

<img width="1075" height="655" alt="image" src="https://github.com/user-attachments/assets/0e9079ac-c787-4fae-9f7c-b5c9ddae4f28" />

### History

History enables users to access their past sessions. Users can view individual, past sessions or a list of all their past sessions, as shown in the image below. Currently sessions are kept until they're manually deleted. When a session is deleted, all data associated with that session is marked as deleted and the time to live (TTL) is set to 30 days. After that TTL expires, queries can't access that data. Logs, which contain session data aren't affected when a session is deleted via the in-product UX. These logs have a retention period of up to 90 days.

<img width="1283" height="683" alt="image" src="https://github.com/user-attachments/assets/5c7a4363-6d2c-422b-870e-e6a1f4f7b6b7" />

### Owner Specific Options

For users configured as owners:

#### Owner Settings

Owner settings. These settings include the option to switch Security Compute Units (SCUs) capacity, select the workspace for Copilot agents, configure data sharing options to help improve Copilot, allow logging audit data in Microsoft Purview, and configure who can upload files.

- Switch capacity
- Agent workspaces
- Improve Copilot
- Audit logging
- File upload

> Swtich capacity
<img width="525" height="319" alt="image" src="https://github.com/user-attachments/assets/345955cc-e898-489a-b1bb-161a9f1ff5e8" />

> Agent workspaces
<img width="733" height="370" alt="image" src="https://github.com/user-attachments/assets/537778d2-5f98-4640-ba5e-473bdfe90dd0" />

> Improve Copilot
<img width="525" height="286" alt="image" src="https://github.com/user-attachments/assets/4b5121f8-ae80-4508-b312-892d3825b885" />

> Audit logging
<img width="603" height="285" alt="image" src="https://github.com/user-attachments/assets/1348f0d8-8a7c-49f5-9d66-d87669f12573" />

> File upload
<img width="434" height="169" alt="image" src="https://github.com/user-attachments/assets/914fc962-2dc7-4e7b-9ad3-c2ee6cd32a39" />

#### Plugin Settings

Plugin settings. Owners configure the following:

- Select who can add and manage their own custom plugins. The available options are Contributors and owners or owners only.
- Select who can add and manage custom plugins for everyone in the organization. The available options are Contributors and owners or owners only.
- Decide which new and existing plugins are available to everyone in your organization, and which are restricted to owners only.
- Allow Security Copilot to access data from your Microsoft 365 services. If you choose not to allow Copilot access, users won't be able to use specific plugins, like Microsoft Purview, or connect any future sources of org knowledge that are housed in Microsoft 365 services.

> Plugin settings
<img width="596" height="646" alt="image" src="https://github.com/user-attachments/assets/2383b80b-47ee-4be4-9ffc-9af296ca436e" />

> Restrict plugin access
<img width="620" height="558" alt="image" src="https://github.com/user-attachments/assets/b9ef74ec-a1e1-4873-8f28-85492d8dc1b4" />

#### Role Assignments

Role assignments, where admins can view and manage existing role assignments for the Copilot Owner and Copilot Contributor roles. This includes the option to add the recommended roles group.

> Role assignment
<img width="1276" height="1547" alt="image" src="https://github.com/user-attachments/assets/860dabe1-8a84-4ae0-9beb-f22ed55b828b" />

> Recommended roles
<img width="591" height="542" alt="image" src="https://github.com/user-attachments/assets/ea396ddd-ea14-43f9-96f8-49487d698de4" />

#### Manage Workspaces

Manage workspaces, where owners can create new workspaces, configure them by assigning access and permissions, and fine-tune settings such as owner roles and plugin configurations. Workspaces are described in more detail in the subsequent unit.

<img width="1285" height="408" alt="image" src="https://github.com/user-attachments/assets/94d2cf9a-f7de-449a-9689-03c165f84347" />

#### Usage Monitoring

Usage monitoring, which provides a dashboard showing how SCUs are consumed over a period of time by your Microsoft Security Copilot workloads. The usage monitoring dashboard provides visibility, for a selected workspace, into the number of units used, the specific plugins employed during sessions, and the initiators of those sessions. The dashboard also allows you to apply filters and export usage data seamlessly. The dashboard includes up to 90 days of data.

When an analyst is in the middle of an investigation and the usage is nearing the provisioned capacity limit (90%), a notification is displayed to the analyst while entering the prompt. The notification informs the analyst to contact the owner to increase the capacity or limit the number of prompts to avoid disruptions. These notifications are also shown in the Security Copilot embedded experiences.

When the provisioned capacity is crossed, the analyst sees an error message stating that due to high usage in organization, they cannot submit additional prompts. The analyst is asked to contact the owner to increase the provisioned SCUs.

> Usage monitoring
<img width="1279" height="846" alt="image" src="https://github.com/user-attachments/assets/15bd3c53-7058-427b-a23c-23a291d636d1" />

> Usage monitoring filters
<img width="1279" height="846" alt="image" src="https://github.com/user-attachments/assets/9b71986e-688f-4a14-8321-517f5168cfab" />

#### Security Store

Security Store, which is integrated into the standalone experience of Microsoft Security Copilot, is Microsoft Security's new security-optimized storefront enabling organizations to find, try, buy, and deploy Microsoft and partner-built security solutions and agents. These solutions and agents integrate directly with Microsoft Security products such as Microsoft Defender, Microsoft Sentinel, Microsoft Entra, Purview, Intune and Security Copilot, offering a unified experience that simplifies procurement and accelerates time to value.

<img width="1344" height="749" alt="image" src="https://github.com/user-attachments/assets/d6db3ddc-9057-428b-bdd0-e0d731e052e5" />

### Settings and Help

Selecting the ellipses on the bottom left corner of the navigation panel, allows users to view settings, access help options, and select a tenant for use with Copilot Studio.

<img width="368" height="619" alt="image" src="https://github.com/user-attachments/assets/6c52fb25-dbf8-4058-8f20-ea9c034f370d" />

#### Settings

Settings, which include configurable preferences, data and privacy statements, and information about the App version.

- **Preferences** - The preferences settings allow users to configure the theme, language, and time zone. Copilot supports many languages. For detailed information, see Supported languages.
- **Data and privacy** - The data and privacy page provides links to the privacy statement, terms and conditions, and location information for where data is stored.
- **About** - The About page provides information of the app version for Copilot.

> Preferences
<img width="890" height="852" alt="image" src="https://github.com/user-attachments/assets/b3d2d31f-46b0-48b9-b5bc-ea84cc0c1318" />

> Data and privacy
<img width="511" height="259" alt="image" src="https://github.com/user-attachments/assets/c0e78fde-1131-4e64-a257-30f853df1f83" />

#### Help

Help enables users to link to documentation and training. If you encounter issues or need to seek assistance, Security Copilot provides an advanced support experience. Depending on your role, the widget allows you to:

- **Find solutions** to common problems. Anyone with access to Security Copilot can access the self help widget by selecting the help icon then selecting the Help tab. Type your question in the prompt bar and articles related to your search will be surfaced.
- **Submit a support case** to the Microsoft support team. To open support cases, you must have, at a minimum, a Service Support Administrator OR Helpdesk Administrator role. You can also view your support history.

> Find solutions
<img width="434" height="852" alt="image" src="https://github.com/user-attachments/assets/147e06cb-a9d2-4e8a-a663-1de00a7497a1" />

> Get support
<img width="580" height="1350" alt="image" src="https://github.com/user-attachments/assets/3bcad953-f0e5-4e13-94e1-fdaa55b3691b" />

#### Tenant Switcher

Tenant switcher. The tenant, which is provisioned for Copilot doesn't need to be the tenant your security analyst logs in from. Also a user may have access to Security Copilot across multiple tenants. In the screenshot that follows, the user is provisioned only in the "Zava - Private" tenant. If the user had been provisioned in other tenants, they would be listed and the user would be able to select any of the available tenants.

<img width="625" height="368" alt="image" src="https://github.com/user-attachments/assets/94f23bc4-9e38-463d-aa91-f1f83b954337" />

---

## Workspaces

Copilot workspaces are separate work environments within the tenant in which your Copilot instance is operating. One way to think about Copilot workspaces is as separate rooms in a house. Each room is configured to be optimized for its function and the people that use that room. The same is true of Copilot workspaces. Admins set up, configure, and manage individual workspaces for specific team needs.

Selecting workspaces opens the drop-down menu where users can select available workspaces to which they have access and set their preferred workspace in cases where they have access to multiple workspaces. Owners will also have the option to manage workspaces, manage capacity usage, and create a new workspace.

More detailed information is provided in a subsequent unit, dedicated to Copilot workspaces.

<img width="329" height="321" alt="image" src="https://github.com/user-attachments/assets/76faafb4-0f24-4de4-9b01-ee2c45de73cf" />

---

## Prompts to Try

Prompts are the primary input Security Copilot needs to generate answers that can help you in your security-related tasks. Promptbooks are a series of prompts that have been put together to accomplish specific security-related tasks.

To help introduce the concept of prompting in Security Copilot, a set of prompts and promptbooks are immediately available on the home screen.

You can apply filters to find prompts or promptbooks that are most relevant to you. Narrow down search results by applying multiple filters to better suit your role or scenario.

Customize your search by selecting filters based on:

- **Roles** - Examples include: CISO, SOC analyst, threat intel analyst, and IT administrator.
- **Plugins** - Examples include: Microsoft Defender XDR, Microsoft Threat Intelligence, and Natural language to KQL for advanced hunting.

You can also use the search function to look up prompts or promptbooks by title.

> Prompts
<img width="875" height="658" alt="image" src="https://github.com/user-attachments/assets/988d809d-e6c6-42e4-8fe1-a768af226f4d" />

> Promptbooks
<img width="876" height="758" alt="image" src="https://github.com/user-attachments/assets/d1df0a9f-b222-403f-a8ab-057a561869c3" />

> Filter by role
<img width="891" height="337" alt="image" src="https://github.com/user-attachments/assets/c580415a-5203-4f45-8ee1-5470da518dee" />

> Filter by plugin
<img width="968" height="424" alt="image" src="https://github.com/user-attachments/assets/1d92c15d-79f2-4b29-a3ba-c06744ff226e" />

---

## Prompt Bar

You use the prompt bar to tell Copilot what insights you want from your security data, in natural language, then select the run icon.

<img width="610" height="78" alt="image" src="https://github.com/user-attachments/assets/4df4b4bd-8096-459b-b2d4-d615260394c8" />

In addition to the run icon, the prompt bar include two other icons:

- Prompt icon
- Sources icon

### Prompt Icon

Select the prompt icon located inside the prompt bar, to open a window where you search for and access promptbooks and system capabilities.

<img width="764" height="578" alt="image" src="https://github.com/user-attachments/assets/1dabd922-9685-4e38-ac48-67b432399a51" />

System capabilities, often referred to as prompt suggestions, are specific, single prompts that you can use in Copilot. The list displayed when you select the prompt icon is a small subset of all the available system capabilities available to you. To view all the system capabilities available to you, select See all system capabilities. The list displayed may vary, depending on the plugins you enabled. There are some capabilities that aren't tied to a specific plugin and as such are available, independent of the enabled plugins, to users with access to Copilot.

Selecting a system capability (prompt suggestion) typically requires more input to get a useful response, but Copilot provides that guidance. As an example, the image that follows shows the information that the user must include to analyze a script or command.

<img width="764" height="182" alt="image" src="https://github.com/user-attachments/assets/0c331d22-73d5-4490-854d-6d3d772aed76" />

### Sources Icon

Copilot integrates with security-specific sources using plugins and files.

- **Plugins** - Copilot currently supports plugins for Microsoft's own security products, non-Microsoft products, open-source intelligence feeds, industry information from the public web, and custom plugins.
- **Files** - Connections to an organization's knowledge bases gives Copilot more context, resulting in responses that are more relevant, specific, and customized to the user. Uploading a file is one approach that Copilot uses to connect to an organization's knowledge base.

You access and manage sources through the sources icon that is included in the prompt bar. The Manage sources window lists the plugins tab (the default view) and the files tab.
<img width="1210" height="578" alt="image" src="https://github.com/user-attachments/assets/2fb9eddd-6c6b-4084-8e95-deb99d84faf3" />

Refer to subsequent units in this module for detailed information on plugins and connection to knowledge bases.

---

## Use Cases and Solutions

### Home Menu Navigation Use Cases

- **Quick access to AI automation** - Security teams need immediate access to AI agents for routine task automation
  - *Solution:* Navigate to Active Agents from the home menu to access Microsoft and non-Microsoft agents, with setup or runtime access depending on role permissions
  - *Reference:* [Microsoft Security Copilot Agents](https://learn.microsoft.com/en-us/copilot-security/agents-security)

- **Standardized investigation procedures** - Teams need consistent, repeatable security investigation workflows
  - *Solution:* Access Promptbooks from the home menu to view builtin and custom promptbooks with descriptions, prompt counts, and ownership information, then select Get started to launch structured investigations
  - *Reference:* [Using Promptbooks in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/using-promptbooks)

- **Custom security agent development** - Organizations need tailored AI agents for specific security scenarios
  - *Solution:* Use the Build (preview) option to extend Security Copilot by building, testing, and publishing custom agents tailored to organizational needs
  - *Reference:* [Build Custom Agents in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/build-agents)

- **Session audit and review** - Analysts need to review past investigations or reference previous findings
  - *Solution:* Access History to view individual past sessions or complete session lists; note that sessions persist until manually deleted with 30-day TTL for data and 90-day retention for logs
  - *Reference:* [Microsoft Security Copilot Session Management](https://learn.microsoft.com/en-us/copilot-security/privacy-data-security)

### Owner Configuration Use Cases

- **Capacity management across workspaces** - Owners need to allocate compute resources efficiently
  - *Solution:* Use Owner settings to switch SCU capacity, configure agent workspaces, and manage data sharing options per workspace
  - *Reference:* [Manage Capacity in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/manage-usage)

- **Controlled plugin ecosystem** - Organizations need governance over which plugins users can access
  - *Solution:* Configure Plugin settings to restrict who can add custom plugins (Contributors and owners vs. owners only), manage organization-wide plugin availability, and control Microsoft 365 data access (required for Purview)
  - *Reference:* [Manage Plugins in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/manage-plugins)

- **Streamlined role assignment** - Admins need efficient ways to grant Copilot access to security teams
  - *Solution:* Use Role assignments to manage Copilot Owner and Contributor roles, with option to add the Recommended Microsoft Security roles group for automatic access to users with existing Microsoft security product permissions
  - *Reference:* [Assign Roles in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/assign-roles)

- **Multi-workspace governance** - Large organizations need isolated environments for different teams
  - *Solution:* Access Manage workspaces to create new workspaces, assign access and permissions, and fine-tune owner roles and plugin configurations per workspace
  - *Reference:* [Workspaces in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/workspaces)

- **Proactive capacity planning** - Organizations need visibility into consumption patterns to prevent service disruption
  - *Solution:* Monitor Usage monitoring dashboard showing SCU consumption, plugin usage, and session initiators with 90-day visibility; analysts receive 90% capacity warnings, enabling owners to increase provisioned SCUs before hard limits are reached
  - *Reference:* [Monitor Usage in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/manage-usage#monitor-usage)

- **Unified security procurement** - Organizations need to discover and deploy integrated security solutions
  - *Solution:* Access Security Store from the home menu to find, try, buy, and deploy Microsoft and partner security solutions that integrate directly with Microsoft Defender, Sentinel, Entra, Purview, Intune, and Security Copilot
  - *Reference:* [Microsoft Security Store](https://learn.microsoft.com/en-us/microsoft-365/security/defender/security-store)

### User Experience Use Cases

- **Personalized interface preferences** - Users need Copilot configured for their locale and accessibility needs
  - *Solution:* Access Settings via the ellipses menu to configure theme, language (see Supported languages), and time zone preferences
  - *Reference:* [Microsoft Security Copilot Supported Languages](https://learn.microsoft.com/en-us/copilot-security/supported-languages)

- **Self-service troubleshooting** - Users encounter issues and need immediate assistance without opening tickets
  - *Solution:* Use Help widget to access self-help documentation and training; search the prompt bar for relevant articles or submit support cases (requires Service Support Administrator or Helpdesk Administrator role)
  - *Reference:* [Get Support for Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/get-support)

- **Multi-tenant security operations** - Security providers or large enterprises work across multiple Copilot tenants
  - *Solution:* Use Tenant switcher to select from available provisioned tenants, enabling access to Security Copilot across multiple organizational boundaries
  - *Reference:* [Understand Authentication in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/understand-authentication)

### Workspace Management Use Cases

- **Team-specific environment selection** - Users have access to multiple workspaces with different configurations
  - *Solution:* Select from the Workspaces drop-down menu to choose available workspaces, set preferred workspace defaults, and access owner options for workspace management and creation
  - *Reference:* [Workspaces in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/workspaces)

### Prompt Discovery Use Cases

- **Role-appropriate security tasks** - Different security roles need relevant starting prompts
  - *Solution:* Apply filters on the home screen by role (CISO, SOC analyst, threat intel analyst, IT administrator) and plugin (Defender XDR, Threat Intelligence, Natural language to KQL) to discover relevant prompts and promptbooks
  - *Reference:* [Prompting in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/prompting-in-copilot)

### Prompt Construction Use Cases

- **Guided complex analysis** - Users need assistance with multi-step security analyses like script examination
  - *Solution:* Click the Prompt icon in the prompt bar to access system capabilities (prompt suggestions); selecting a capability provides guided input requirements, such as specific fields needed for script analysis
  - *Reference:* [System Capabilities in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/prompting-in-copilot)

- **Knowledge-augmented investigations** - Investigations require organizational context beyond built-in data sources
  - *Solution:* Click the Sources icon in the prompt bar to manage plugins (Microsoft, non-Microsoft, open-source, public web, custom) and upload files to connect organizational knowledge bases for more relevant, specific responses
  - *Reference:* [Manage Sources in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/manage-plugins)

---

## References

- [Microsoft Security Copilot Documentation](https://learn.microsoft.com/en-us/copilot/security/)
- [Understand Authentication in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/understand-authentication)
- [Assign Roles in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/assign-roles)
- [Workspaces in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/workspaces)
- [Manage Capacity and Usage](https://learn.microsoft.com/en-us/copilot-security/manage-usage)
- [Manage Plugins in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/manage-plugins)
- [Using Promptbooks](https://learn.microsoft.com/en-us/copilot-security/using-promptbooks)
- [Prompting in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/prompting-in-copilot)
- [Microsoft Security Copilot Agents](https://learn.microsoft.com/en-us/copilot-security/agents-security)
- [Build Custom Agents](https://learn.microsoft.com/en-us/copilot-security/build-agents)
- [Microsoft Security Store](https://learn.microsoft.com/en-us/microsoft-365/security/defender/security-store)
- [Supported Languages](https://learn.microsoft.com/en-us/copilot-security/supported-languages)
- [Get Support](https://learn.microsoft.com/en-us/copilot-security/get-support)
- [Data Privacy and Security](https://learn.microsoft.com/en-us/copilot-security/privacy-data-security)
