# Describe the Microsoft Plugins Available in Microsoft Security Copilot

Microsoft Security Copilot integrates with various sources, including Microsoft's own security products, non-Microsoft vendors, open-source intelligence feeds, websites, and knowledge bases to generate guidance that's specific to your organization.

One of the mechanisms by which Copilot integrates to these various sources is through plugins. Plugins extend Copilot's capabilities. In this unit, you'll explore the Microsoft plugins.

---

## Microsoft Plugins

Microsoft plugins give Copilot access to information and capabilities from within your organization's Microsoft products. The image that follows shows only a subset of the available Microsoft plugins and the order in which the plugins are listed may vary from what is displayed in the product.

If a Copilot owner has restricted plugin access, then those plugins that have been set to restricted will show greyed out and restricted.

> Plugins
<img width="530" height="489" alt="image" src="https://github.com/user-attachments/assets/5d67654f-ea18-4923-8453-0f4fb36bcda2" />

> Restricted plugins
<img width="520" height="353" alt="image" src="https://github.com/user-attachments/assets/244b02f4-2383-4fec-a57d-69a33bdf9757" />

Generally speaking, Microsoft plugins in Copilot use the OBO (on behalf of) model – meaning that Copilot knows that a customer has licenses to specific products and is automatically signed into those products. Copilot can then access the specific products when the plugin is enabled and, where applicable, parameters are configured. Some Microsoft plugins that require setup, as noted by the settings icon or the setup button, may include configurable parameters that are used for authentication in-lieu of the OBO model.

To view the system capabilities supported by the enabled plugins, you select the prompt icon located in the prompt bar and select "See all system capabilities." System capabilities are specific, single prompts that you can use in Copilot. Selecting a system capability typically requires more input to get a useful response, but Copilot provides that guidance.

<img width="790" height="448" alt="image" src="https://github.com/user-attachments/assets/4809dae4-6da0-42ba-859b-5251afd694de" />

The sections that follow provide brief descriptions for many, but not all, of the available Microsoft plugins. Microsoft Security Copilot is continually adding support for Microsoft products.

---

## Azure Firewall (Preview)

Azure Firewall is a cloud-native and intelligent network firewall security service that provides best of breed threat protection for your cloud workloads running in Azure. It's a fully stateful firewall as a service with built-in high availability and unrestricted cloud scalability.

The Azure Firewall integration with Copilot helps analysts perform detailed investigations of the malicious traffic intercepted by the intrusion detection and prevention system (IDPS) and/or the threat intelligence capabilities of the firewalls across their environment.

To use the Azure Firewall integration with Copilot:

- The Azure Firewalls to be used with Security Copilot must be configured with resource specific structured logs for IDPS and these logs must be sent to a Log Analytics workspace.
- The users using the Azure Firewall plugin in Security Copilot must have the appropriate Azure role-based access control (RBAC) roles to access the Firewall and associated Log Analytics workspace.
- The Azure Firewall plugin in Security Copilot must be turned on.

Azure Firewall capabilities in Copilot are built-in prompts that you can use but you can also enter your own prompts based on the capabilities supported.

<img width="488" height="244" alt="image" src="https://github.com/user-attachments/assets/94517327-c423-4e9c-a5b2-4a021271f993" />

Example prompts include:

- Has there been any malicious traffic intercepted by my Firewall &lt;Firewall name&gt;?
- What are the top 20 IDPS hits from the last seven days for Firewall &lt;Firewall name&gt; in resource group &lt;resource group name&gt;?
- If I want to make sure all my Firewalls are protected against attacks from signature ID &lt;ID number&gt;, how do I do this?

---

## Azure Web Application Firewall (Preview)

Azure Web Application Firewall (WAF) integration in Security Copilot enables deep investigation of Azure WAF events. It can help you investigate WAF logs triggered by Azure WAF in a matter of minutes and provide related attack vectors using natural language responses at machine speed. It provides visibility into your environment's threat landscape. It allows you to retrieve a list of most frequently triggered WAF rules and identify the top offending IP addresses in your environment.

Security Copilot integration is supported on both Azure WAF integrated with Azure Application Gateway and Azure WAF integrated with Azure Front Door.

To use the Azure WAF integration in Copilot, the Azure WAF plugin in Security Copilot must be turned on and configured.

The preview standalone experience in Azure WAF can help you with:

- Providing a list of top Azure WAF rules triggered in the customer environment and generating deep context with related attack vectors.
- Providing a list of malicious IP addresses in the customer environment and generating related threats.
- Summarizing SQL injection(SQLi) attacks.
- Summarizing Cross-site scripting(XSS) attacks.

Azure Web Application Firewall capabilities in Copilot are built-in prompts that you can use but you can also enter your own prompts based on the capabilities supported.

<img width="552" height="221" alt="image" src="https://github.com/user-attachments/assets/35a3981e-fcdf-4e57-98cb-ae19bb0eaf13" />

Example prompts include:

- Was there a SQL injection attack in my global WAF in the last day?
- What were the top global WAF rules triggered in the last 24 hours?
- Summarize list of malicious IP addresses in my Azure Front Door WAF in the last six hours?

---

## Azure AI Search (Preview)

The Azure AI Search plugin allows you to connect your company's knowledge bases or repositories to Microsoft Security Copilot. Details on this plugin and connections to knowledge bases are described in a subsequent unit of this module.

---

## Microsoft Entra

Microsoft Entra is a family of multicloud identity and network access solutions that enables organizations to protect any identity and secure access to any resource. It provides a unified platform for identity and network access management, making it easier to secure identities and access to resources across multicloud and hybrid environments.

Security Copilot integrates with Microsoft Entra. With the Entra plugin enabled, security analysts can instantly get a risk summary, steps to remediate, and recommended guidance for each identity at risk, in natural language. Analysts can use Copilot to guide in the creation of a lifecycle workflow to streamline the process of creating and issuing user credentials and access rights. These and many other Entra capabilities are supported by Copilot.

Microsoft Entra capabilities in Copilot are built-in prompts that you can use but you can also enter your own prompts based on the capabilities supported.

<img width="708" height="442" alt="image" src="https://github.com/user-attachments/assets/44d612e9-3c25-4305-a48b-3eca6317e798" />

With the plugin enabled, Copilot integration with Microsoft Entra can also be experienced through the embedded experience. The scenarios supported through the embedded experience are described in more detail in the module titled, "Describe the embedded experiences of Microsoft Security Copilot."

---

## Microsoft Intune

Microsoft Intune is a cloud-based endpoint management solution. It manages user access to organizational resources and simplifies app and device management across your many devices, including mobile devices, desktop computers, and virtual endpoints.

Security Copilot integrates with Microsoft Intune. If Microsoft Intune is available in the same tenant as Copilot and the plugin is enabled, Copilot will be able to get information about your devices, apps, compliance & configuration policies, and policy assignments managed in Intune.

To utilize the Microsoft Intune plugin, the user would need to be assigned an Intune service-specific role like the Intune Endpoint Security Manager role in addition to the role permission that grants access to Copilot.

Capabilities supported by the Intune plugin enable a user to:

- Compare different security baselines.
- Get a summary of an existing policy.
- Get policy assignment scope.
- Get the differences or comparisons between two devices.
- Quickly gather details for a device by asking about it.
- Get detailed information about a user's device enrollments and device compliance for troubleshooting or a security investigation.
- And more

Microsoft Intune capabilities in Copilot are built-in prompts that you can use, but you can also enter your own prompts based on the capabilities supported

<img width="704" height="444" alt="image" src="https://github.com/user-attachments/assets/f10173a2-4a50-487b-9cf6-1f26aae66bc6" />

Some sample prompts include:

- What Intune apps are assigned the most?
- How many devices were enrolled in Intune in the last 24 hours?
- What is the hardware configuration difference between the DeviceA and DeviceB devices?

With the plugin enabled, Copilot integration with Microsoft Intune can also be experienced through the embedded experience. The scenarios supported through the embedded experience are described in more detail in the module titled, "Describe the embedded experiences of Microsoft Security Copilot."

---

## Microsoft Defender XDR

Microsoft Defender XDR is a unified pre- and post-breach enterprise defense suite that natively coordinates detection, prevention, investigation, and response across endpoints, identities, email, and applications to provide integrated protection against sophisticated attacks.

There are two separate plugins in Copilot that relate to Microsoft Defender XDR (the user interface may still show Microsoft 365 Defender):

- Microsoft Defender XDR
- Natural language to KQL for Microsoft Defender XDR

The role permission that grants the user access to Copilot determines the level of access to Microsoft Defender XDR data. There are no additional role permissions required to use the Microsoft Defender XDR plugin or the Natural language to Defender XDR KQL plugin.

### Microsoft Defender XDR

The Microsoft Defender XDR plugin includes capabilities that enable users to:

- Summarize incidents quickly
- Take action on incidents through guided responses.
- Create incident reports
- Get incident guided responses
- Get Defender device summaries
- Analyze files
- more...

Microsoft Defender XDR capabilities in Copilot are built-in prompts that you can use, but you can also enter your own prompts based on the capabilities supported.

<img width="698" height="366" alt="image" src="https://github.com/user-attachments/assets/388e031e-65ab-45f4-a703-0e4a37ac633f" />

Copilot also includes a builtin promptbook for Microsoft Defender XDR incident investigation you can use to get a report about a specific incident, with related alerts, reputation scores, users, and devices.

With the plugin enabled, Copilot integration with Defender XDR can also be experienced through the embedded experience. The scenarios supported through the embedded experience are described in more detail in the module titled, "Describe the embedded experiences of Microsoft Security Copilot."

### Natural Language to KQL for Microsoft Defender

The Natural language to KQL for Microsoft Defender (NL2KQLDefender) plugin enables query assistant functionality that converts any natural-language question in the context of threat hunting, into a ready-to-run KQL query. The query assistant saves security teams time by generating a KQL query that can then be automatically run or further tweaked according to the analyst's needs.

---

## Microsoft Defender External Attack Surface Management (Defender EASM)

Microsoft Defender External Attack Surface Management (Defender EASM) continuously discovers and maps your digital attack surface to provide an external view of your online infrastructure. This visibility enables security and IT teams to identify unknowns, prioritize risk, eliminate threats, and extend vulnerability and exposure control beyond the firewall. Attack Surface Insights are generated by using vulnerability and infrastructure data to showcase the key areas of concern for your organization.

If you use Defender EASM in the same tenant as Copilot and enable the plugin, Copilot can surface insights from Defender EASM about an organization's attack surface. These insights can help you understand your security posture and mitigate vulnerabilities.

Defender EASM capabilities in Copilot are built-in prompts that you can use, but you can also enter your own prompts based on the capabilities supported.

<img width="706" height="448" alt="image" src="https://github.com/user-attachments/assets/392638a8-db08-4317-930f-1766a86921b6" />

Some example prompts include:

- Is my external attack surface impacted by CVE-2023-21709?
- Get assets affected by high priority CVSSs in my attack surface.
- How many assets have critical CVSSs for my organization?

To use this plugin, it's necessary to configure parameters to identify your organization's subscription to Defender EASM.

<img width="944" height="450" alt="image" src="https://github.com/user-attachments/assets/f9b6b100-5a20-481e-b38e-e8992d7c4402" />

---

## Microsoft Defender Threat Intelligence

Microsoft Defender Threat Intelligence (Defender TI) is a platform that streamlines triage, incident response, threat hunting, vulnerability management, and cyber threat intelligence analyst workflows when conducting threat infrastructure analysis and gathering threat intelligence.

Security Copilot integrates with Microsoft Defender TI. With the Defender TI plugin enabled, Copilot delivers information about threat activity groups, indicators of compromise (IOCs), tools, and contextual threat intelligence. You can use the prompts and promptbooks to investigate incidents, enrich your hunting flows with threat intelligence information, or gain more knowledge about your organization's or the global threat landscape.

Microsoft Defender TI capabilities in Copilot are built-in prompts that you can use, but you can also enter your own prompts based on the capabilities supported.

<img width="604" height="448" alt="image" src="https://github.com/user-attachments/assets/cd2ec887-e5ee-4157-ba2a-cb0f000be931" />

Some sample prompts include:

- Show me the latest threat articles.
- Get threat articles associated with the finance industry.
- Share the technologies that are susceptible to the vulnerability - CVE-2021-44228.
- Summarize the vulnerability CVE-2021-44228.

Builtin promptbooks that deliver information from Defender TI, include:

- Vulnerability impact assessment - Generates a report summarizing the intelligence for a known vulnerability, including steps on how to address it.
- Threat actor profile - Generates a report profiling a known activity group, including suggestions to defend against their common tools and tactics.

---

## Microsoft Purview

Microsoft Purview is a comprehensive set of solutions that can help your organization govern, protect, and manage data, wherever it lives. Microsoft Purview solutions provide integrated coverage and help address the fragmentation of data across organizations, the lack of visibility that hampers data protection and governance, and the blurring of traditional IT management roles.

The Purview plugin in Security Copilot, enables you to gain valuable data and user risk insights to help identify the source of an attack and any sensitive data that may be at risk, provided you have the appropriate role permission within Microsoft Purview. Because Microsoft Copilot assumes the permissions of the user when it tries to access the data to answer the queries, you need to have the required role permissions to access the data. Also, your organization must be licensed and onboarded to the applicable Microsoft Purview solutions.

Microsoft Purview capabilities in Copilot are built-in prompts that you can use, but you can also enter your own prompts based on the capabilities supported.

<img width="606" height="444" alt="image" src="https://github.com/user-attachments/assets/d51c3b58-44c1-4254-9b36-dc36e131a28d" />

Copilot capabilities can also be experienced directly from within Purview solutions, through the embedded experience. The scenarios supported through the embedded experience are described in more detail in the module titled, "Describe the embedded experiences of Microsoft Security Copilot."

---

## Microsoft Sentinel (Preview)

Microsoft Sentinel delivers intelligent security analytics and threat intelligence across the enterprise. With Microsoft Sentinel, you get a single solution for attack detection, threat visibility, proactive hunting, and threat response.

There are two separate plugins in Copilot that relate to Sentinel:

- Microsoft Sentinel (Preview)
- Natural language to Microsoft Sentinel KQL (Preview)

<img width="606" height="375" alt="image" src="https://github.com/user-attachments/assets/fff635b3-b542-4126-91fe-c857af65e3ff" />

### Microsoft Sentinel (Preview)

To utilize the Sentinel plugin, the user would need to be assigned a role permission that grants access to Copilot and a Sentinel specific role like Microsoft Sentinel Reader to access incidents in the workspace.

The Sentinel plugin also requires the user to configure the Sentinel workspace, the subscription name, and the resource group name.

<img width="850" height="423" alt="image" src="https://github.com/user-attachments/assets/ec5949b3-ee12-44ab-9a7e-60a7588a174c" />

The Sentinel plugin capabilities are focused on incidents and workspaces. Additionally, Copilot includes a promptbook for Microsoft Sentinel incident investigation. This promptbook includes prompts for getting a report about a specific incident, along with related alerts, reputation scores, users, and devices.

### Natural Language to Microsoft Sentinel KQL (Preview)

The natural language to Sentinel KQL (NL2KQLSentinel) plugin converts any natural-language question in the context of threat hunting, into a ready-to-run KQL query. This saves security teams time by generating a KQL query that can then be automatically run or further tweaked according to the analyst's needs.

---

## Use Cases and Solutions

### Azure Firewall Use Cases

- **Malicious traffic investigation** - Security teams need to analyze IDPS alerts across multiple Azure Firewalls efficiently
  - *Solution:* Enable the Azure Firewall plugin with resource-specific structured logs sent to Log Analytics, then use natural language prompts to investigate malicious traffic, retrieve top IDPS hits, and verify protection against specific signature IDs
  - *Reference:* [Azure Firewall Plugin in Security Copilot](https://learn.microsoft.com/en-us/copilot-security/azure-firewall-plugin)

### Azure Web Application Firewall Use Cases

- **Rapid WAF event investigation** - Analysts need to quickly understand WAF triggers and attack patterns
  - *Solution:* Turn on and configure the Azure WAF plugin for Application Gateway or Front Door, then use built-in prompts to get top triggered rules, identify malicious IPs, and summarize SQL injection or XSS attacks within minutes
  - *Reference:* [Azure WAF Integration with Security Copilot](https://learn.microsoft.com/en-us/copilot-security/azure-waf-plugin)

### Microsoft Entra Use Cases

- **Identity risk remediation** - Security teams need to understand and remediate identity-based risks quickly
  - *Solution:* Enable the Entra plugin to get instant risk summaries, remediation steps, and natural language guidance for at-risk identities, plus create lifecycle workflows for streamlined credential management
  - *Reference:* [Microsoft Entra Plugin in Security Copilot](https://learn.microsoft.com/en-us/copilot-security/entra-plugin)

### Microsoft Intune Use Cases

- **Endpoint security comparison** - IT teams need to compare device configurations and policy assignments
  - *Solution:* With Intune Endpoint Security Manager role and Copilot access, use the Intune plugin to compare security baselines, get policy summaries and assignment scopes, and analyze hardware configuration differences between devices
  - *Reference:* [Microsoft Intune Plugin in Security Copilot](https://learn.microsoft.com/en-us/copilot-security/intune-plugin)

### Microsoft Defender XDR Use Cases

- **Incident response acceleration** - SOC analysts need to quickly understand and act on complex incidents
  - *Solution:* Use the Defender XDR plugin to summarize incidents, get guided responses, create incident reports, and analyze files; leverage the NL2KQLDefender plugin to convert natural language hunting questions into ready-to-run KQL queries
  - *Reference:* [Microsoft Defender XDR Plugin](https://learn.microsoft.com/en-us/copilot-security/defender-xdr-plugin)

### Defender EASM Use Cases

- **External attack surface assessment** - Security teams need to understand exposure to specific vulnerabilities
  - *Solution:* Configure the Defender EASM plugin with subscription parameters, then query for CVE impact on external assets, retrieve high-priority CVSS-affected assets, and get critical vulnerability counts for the organization
  - *Reference:* [Defender EASM Plugin in Security Copilot](https://learn.microsoft.com/en-us/copilot-security/defender-easm-plugin)

### Microsoft Defender Threat Intelligence Use Cases

- **Threat intelligence enrichment** - Analysts need contextual threat data for investigations
  - *Solution:* Enable the Defender TI plugin to access threat articles by industry, get vulnerability summaries (e.g., CVE-2021-44228), and use builtin promptbooks for vulnerability impact assessments and threat actor profiling
  - *Reference:* [Defender Threat Intelligence Plugin](https://learn.microsoft.com/en-us/copilot-security/defender-ti-plugin)

### Microsoft Purview Use Cases

- **Data risk investigation** - Security teams need to identify sensitive data exposure during incident response
  - *Solution:* With appropriate Purview roles and licensing, use the Purview plugin to gain data and user risk insights, identify attack sources, and determine sensitive data at risk during security investigations
  - *Reference:* [Microsoft Purview Plugin in Security Copilot](https://learn.microsoft.com/en-us/copilot-security/purview-plugin)

### Microsoft Sentinel Use Cases

- **SIEM incident investigation** - Analysts need to investigate Sentinel incidents without writing complex queries
  - *Solution:* Configure the Sentinel plugin with workspace, subscription, and resource group details; use builtin prompts and the incident investigation promptbook for comprehensive incident reports, plus leverage NL2KQLSentinel to generate KQL queries from natural language hunting questions
  - *Reference:* [Microsoft Sentinel Plugin in Security Copilot](https://learn.microsoft.com/en-us/copilot-security/sentinel-plugin)

### Plugin Management Use Cases

- **Restricted plugin access** - Organizations need to control which plugins users can access
  - *Solution:* Owners can restrict plugin access, causing restricted plugins to appear greyed out; users access enabled plugins via the prompt icon to view system capabilities ("See all system capabilities") with guidance on required inputs

- **OBO authentication issues** - Some Microsoft products require explicit authentication rather than automatic OBO
  - *Solution:* For plugins marked with settings icons or setup buttons, configure the required parameters for authentication in-lieu of the OBO model, then access product-specific capabilities

---

## References

- [Microsoft Security Copilot Plugins Overview](https://learn.microsoft.com/en-us/copilot-security/manage-plugins)
- [Azure Firewall Plugin](https://learn.microsoft.com/en-us/copilot-security/azure-firewall-plugin)
- [Azure Web Application Firewall Plugin](https://learn.microsoft.com/en-us/copilot-security/azure-waf-plugin)
- [Microsoft Entra Plugin](https://learn.microsoft.com/en-us/copilot-security/entra-plugin)
- [Microsoft Intune Plugin](https://learn.microsoft.com/en-us/copilot-security/intune-plugin)
- [Microsoft Defender XDR Plugin](https://learn.microsoft.com/en-us/copilot-security/defender-xdr-plugin)
- [Defender External Attack Surface Management Plugin](https://learn.microsoft.com/en-us/copilot-security/defender-easm-plugin)
- [Microsoft Defender Threat Intelligence Plugin](https://learn.microsoft.com/en-us/copilot-security/defender-ti-plugin)
- [Microsoft Purview Plugin](https://learn.microsoft.com/en-us/copilot-security/purview-plugin)
- [Microsoft Sentinel Plugin](https://learn.microsoft.com/en-us/copilot-security/sentinel-plugin)
- [Natural Language to KQL in Defender](https://learn.microsoft.com/en-us/copilot-security/nl2kql-defender)
- [Natural Language to KQL in Sentinel](https://learn.microsoft.com/en-us/copilot-security/nl2kql-sentinel)
- [Describe Embedded Experiences](https://learn.microsoft.com/en-us/copilot-security/describe-embedded-experiences)
