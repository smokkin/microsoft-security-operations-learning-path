# Describe Microsoft Security Copilot Terminology

## Terminology

The following terms are important for understanding the way Microsoft Security Copilot works:

- **Session** – A particular conversation within Copilot. Copilot maintains context within a session.
- **Prompt** – A specific statement or question within a session. A user enters a prompt in the prompt bar.
- **Capability** – A function Copilot uses to solve part of a problem. A capability may sometimes be referred to as a skill.
- **Plugin** – A collection of capabilities by a particular resource.
- **Workspace** - Copilot workspaces are separate Copilot work environments within the tenant in which your Copilot instance is operating.
- **Agents** - Microsoft Security Copilot agents are AI-powered tools that autonomously manage security and IT tasks, enhancing threat response, reducing manual workloads, and improving efficiency across cybersecurity operations at scale.
- **Orchestrator** – Copilot's system for composing capabilities together to answer a user's prompt.

---

## Prompt Bar and Sessions

At the center of Security Copilot is the prompt bar. You use the prompt bar to tell Copilot what insights you want from your security data, this is referred to as the prompt. In other words, the prompt is the text-based, natural language input you provide in the prompt bar that instructs Copilot to generate a response. Although you interact with Copilot in natural language, it's helpful to be specific in the prompts (specific questions or statements) that you provide. For those that are relatively new to the security analyst role and engaging with AI, effective prompting may take some practice. For this reason, Copilot provides promptbooks that provide a series of preselected prompts and prompt suggestions (more details on this in a subsequent module).

As you make requests and as Copilot responds, you may have some follow-up requests. The entirety of the dialog is referred to as a session. Copilot maintains context within a session.

<img width="525" height="452" alt="image" src="https://github.com/user-attachments/assets/25bba8fd-50de-47d6-bf43-c974c5f7e5b4" />

---

## Plugins and Capabilities

In the previous unit, we mentioned that Copilot integrates with various sources through plugins, including Microsoft's own security products such as Microsoft Sentinel, Microsoft Defender XDR, and Microsoft Intune, non-Microsoft solutions, and open-source intelligence feeds. The integration enabled by the plugin, for any specific data source, provides Copilot with a collection of capabilities. Each capability is like a function in software, it's designed to do a specialized task within the scope of the data source.

For example, the plugin to Microsoft Defender XDR includes a collection of individual capabilities that are used only by Microsoft Defender XDR. These include:

- The ability to summarize an incident.
- Support incident response teams in resolving incidents through guided responses (a set of recommended actions based on the specific incident).
- The ability to analyze scripts and code.
- The ability to generate KQL queries from natural language input.
- The ability to generate incident reports.

A plugin for Microsoft Sentinel may have similar capabilities but runs only within the scope of Microsoft Sentinel.

Copilot currently supports plug-ins for Microsoft services and non-Microsoft services, including websites and custom plug-ins that can be enabled.

<img width="526" height="452" alt="image" src="https://github.com/user-attachments/assets/88d68799-441d-47ef-bd38-029f560b4ec5" />

<img width="525" height="452" alt="image" src="https://github.com/user-attachments/assets/765ba4db-b148-4890-9a09-0df76b683513" />

Some plugins require setup and configuration, as depicted by the Setup button or the gear icon. For Microsoft plugins, set up may be required where resource specific information needs to be specified. For non-Microsoft sources, set up may be required for account authentication.

---

## Workspaces

Copilot workspaces are separate Copilot work environments within the tenant in which your Copilot instance is operating.

To help you better understand the concept of workspaces, we'll use the analogy of house with multiple rooms. Each room is configured to be optimized for its function and the people that will use that room. When someone enters the house, they may have access to some rooms but not others.

You can think of Copilot Workspaces fitting into this analogy. A Copilot workspace is analogous to a room in a house. You can also think of the house as analogous to a tenant. In the same way that a house has multiple rooms, the tenant in which Copilot is operating can have multiple workspaces.

<img width="525" height="452" alt="image" src="https://github.com/user-attachments/assets/26a8902f-05b2-412c-9b29-f0d645738641" />

Through the tenant-switching capability in Security Copilot, a user can select in which tenant they'll be working. In our analogy, this is a Copilot user getting access to the house. Once the tenant is selected, a Copilot user can access and work in any workspace (room in the house) to which they have access, within the context of their role permissions in that workspace.

Workspaces are powered by capacities and each workspace must have its own capacity.

Using workspaces, you can efficiently map and monitor costs based on team needs and budgets, ensuring that teams have the capacity they need and resources are allocated effectively. Having workspaces also allows you to store session data according to geo-specific regulations and adhere to local data protection laws. These are just a few of the benefits of using workspaces.

For more information, see "Describe workspaces", which is linked in the Summary and resource section of this module.

---

## Agents

A Microsoft Security Copilot agent is an advanced, AI-powered assistant built into Microsoft Security Copilot. These agents go beyond just answering questions—they can autonomously manage high-volume security and IT tasks. They're deeply integrated with Microsoft's security tools and can also work with partner solutions. Each agent is tailored for specific security scenarios, such as threat protection, identity management, or data security.

These agents are designed to learn from feedback, adapt to your organization's workflows, and operate securely within Microsoft's Zero Trust framework. See the summary and resources unit for links to more information on Microsoft Security Copilot agents.

<img width="525" height="652" alt="image" src="https://github.com/user-attachments/assets/0a2b9582-0659-4b53-9fe2-05b93932d816" />

---

## Orchestrator

The orchestrator is Copilot's system for composing capabilities together to answer a user's prompt. This function is illustrated in more detail in the subsequent unit that describes how Copilot processes prompt requests.

---

## Use Cases and Solutions

### Session and Prompt Management Use Cases

- **Maintaining conversation context** - Security analysts need to ask follow-up questions without re-explaining the entire investigation context
  - *Solution:* Use sessions which maintain context throughout the dialog, allowing analysts to build on previous prompts and responses naturally

- **Effective prompting for new analysts** - Junior security analysts struggle to formulate effective natural language queries for AI assistance
  - *Solution:* Leverage promptbooks that provide preselected prompts and prompt suggestions to guide users in crafting specific, effective questions or statements

### Plugin and Capability Use Cases

- **Incident investigation in Defender XDR** - Analysts need to quickly understand and respond to security incidents without manual script analysis
  - *Solution:* Use the Microsoft Defender XDR plugin capabilities to summarize incidents, analyze scripts and code, generate KQL queries from natural language, and provide guided response recommendations

- **Cross-platform security integration** - Organizations use both Microsoft and non-Microsoft security tools requiring unified Copilot access
  - *Solution:* Enable plugins for both Microsoft services (Sentinel, Intune, Defender XDR) and non-Microsoft services (ServiceNow, Splunk, public web, custom plugins), with appropriate setup and authentication configuration

- **Custom security data source integration** - Organizations need Copilot to access proprietary or industry-specific threat intelligence
  - *Solution:* Configure custom plugins that can be enabled to integrate with specific organizational data sources and open-source intelligence feeds

### Workspace Management Use Cases

- **Cost allocation across security teams** - Organizations need to track and budget Copilot usage by department or function
  - *Solution:* Create separate workspaces powered by individual capacities to efficiently map and monitor costs based on team needs and budgets

- **Data residency compliance** - Organizations must store security session data in specific geographic regions to meet regulatory requirements
  - *Solution:* Configure workspaces to store session data according to geo-specific regulations and adhere to local data protection laws

- **Role-based access control** - Different security team members need access to different Copilot environments based on responsibilities
  - *Solution:* Implement workspaces with role permissions, allowing users to access only specific workspaces within the tenant based on their assigned roles

- **Multi-tenant security operations** - Security providers manage multiple client organizations requiring isolated environments
  - *Solution:* Use tenant-switching capability to select the appropriate tenant, then access assigned workspaces within that tenant context

### Agent Deployment Use Cases

- **High-volume security task automation** - Security teams are overwhelmed with repetitive manual tasks across threat protection, identity, and data security
  - *Solution:* Deploy Microsoft Security Copilot agents that autonomously manage high-volume security and IT tasks, learning from feedback and adapting to organizational workflows within the Zero Trust framework

- **Integrated security operations** - Organizations need AI assistance that works seamlessly across Microsoft security tools and partner solutions
  - *Solution:* Use agents tailored for specific security scenarios that are deeply integrated with Microsoft's security tools and capable of working with partner solutions

### Orchestration Use Cases

- **Complex multi-step security queries** - Analysts need answers that require combining multiple specialized functions across different data sources
  - *Solution:* The orchestrator automatically composes relevant capabilities together to answer user prompts, eliminating the need for analysts to manually coordinate multiple tools

---

## References

- [Microsoft Security Copilot Documentation](https://learn.microsoft.com/en-us/copilot/security/)
- [Microsoft Security Copilot Terminology](https://learn.microsoft.com/en-us/copilot/security/copilot-security-terminology)
- [Microsoft Security Copilot Workspaces](https://learn.microsoft.com/en-us/copilot/security/workspaces)
- [Microsoft Security Copilot Plugins](https://learn.microsoft.com/en-us/copilot/security/manage-plugins)
- [Microsoft Security Copilot Agents](https://learn.microsoft.com/en-us/copilot/security/agents-security)
- [Microsoft Defender XDR Integration](https://learn.microsoft.com/en-us/defender-xdr/security-copilot-in-microsoft-365-defender)
- [Microsoft Sentinel Integration](https://learn.microsoft.com/en-us/azure/sentinel/copilot-in-sentinel)
- [Azure OpenAI Service Documentation](https://learn.microsoft.com/en-us/azure/ai-services/openai/)
