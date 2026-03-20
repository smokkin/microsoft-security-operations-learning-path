# Describe the Non-Microsoft Plugins Supported by Microsoft Security Copilot

Microsoft Security Copilot supports non-Microsoft plugins to extend Copilot's capabilities. These plugins are categorized as:

- Other
- Websites
- Custom

---

## Other Plugins

Other plugins give Copilot access to information and capabilities from services beyond Microsoft that your organization uses.

If a Copilot owner has restricted plugin access, then those plugins that have been set to restricted will show greyed out and restricted.

<img width="484" height="886" alt="image" src="https://github.com/user-attachments/assets/ccaead66-3de2-4dd8-b11a-5fe4f3534eb7" />

The list of Other plugins currently supported is long and continually growing. The list that follows is only a subset of non-Microsoft Plugins currently in preview with Copilot.

- CIRCL Hash Lookup (Preview)
- Security Copilot Plugin for ServiceNow (Preview)
- Security Copilot Plugin for Splunk (Preview)
- CrowdSec Threat Intelligence (Preview)
- GreyNoise Community (Preview)
- GreyNoise Enterprise (Preview)

Access to these plugins assumes an account and license to the specific service and a setup that includes authentication. The type of authentication required is determined by the plugin provided. For example, the CrowdSec Threat Intelligence plugin requires an access identifier for API authentication.

<img width="656" height="306" alt="image" src="https://github.com/user-attachments/assets/b02ad012-94fd-47a4-980d-218f991df6bc" />

---

## Websites

The websites plugins give Copilot access to industry information from the public web. Currently, the public web plugin is supported. More website plugins are expected.

The website plugins are accessed using anonymous authentication.

<img width="484" height="148" alt="image" src="https://github.com/user-attachments/assets/02c05fa7-6149-4acd-bc31-4360aa5ecf69" />

---

## Custom

The Microsoft Security Copilot platform enables developers and users to write their own plugins that can be invoked to perform specialized tasks.

<img width="484" height="270" alt="image" src="https://github.com/user-attachments/assets/663b3dc4-6614-417a-bcc2-650e4e46b316" />

There are two types of custom plugins:

- Custom Copilot plugins that you develop
- Custom plugins developed with OpenAI's API.

Regardless of the approach, every Copilot plugin requires a YAML or JSON formatted manifest file (for example: plugin.yaml or plugin.json) which describes metadata about the skill set and how to invoke the skills.

Owner settings, described in a previous unit, determines who can add and manage their own custom plugins and who can add and manage custom plugins for everyone in the organization. For Copilot users with the contributor role, availability of the option to set "Who can use this plugin" is dependent on how the owner settings for custom plugins are configured.

<img width="674" height="350" alt="image" src="https://github.com/user-attachments/assets/85fd1840-fa70-42e8-82f0-39aa22f739fe" />

Once a custom plugin is added, it can be turned on or off, updated, or deleted.

To Learn more about custom plugins, see Create your own custom plugins.

Watch this short video for a summary on setting up non-Microsoft plugins.

---

## Use Cases and Solutions

### Third-Party Integration Use Cases

- **Threat intelligence enrichment** - Security teams need to correlate internal alerts with external threat intelligence sources
  - *Solution:* Enable the CrowdSec Threat Intelligence, GreyNoise Community, or GreyNoise Enterprise plugins with appropriate API authentication to enrich investigations with external threat data
  - *Reference:* [CrowdSec Plugin for Security Copilot](https://learn.microsoft.com/en-us/copilot-security/crowdsec-plugin)

- **Hash verification and analysis** - Analysts need to verify file hashes against known databases during malware investigations
  - *Solution:* Configure the CIRCL Hash Lookup plugin to access hash reputation data from CIRCL's database, providing additional context for file analysis
  - *Reference:* [CIRCL Hash Lookup Plugin](https://learn.microsoft.com/en-us/copilot-security/circl-hash-plugin)

- **IT service management integration** - Security incidents need to trigger workflows in existing ITSM platforms
  - *Solution:* Set up the ServiceNow plugin with account credentials and authentication to enable bidirectional integration between Security Copilot and ServiceNow for incident management
  - *Reference:* [ServiceNow Plugin for Security Copilot](https://learn.microsoft.com/en-us/copilot-security/servicenow-plugin)

- **SIEM data correlation** - Organizations need to query Splunk data through natural language in Copilot
  - *Solution:* Enable the Splunk plugin with proper authentication to allow Copilot to access and query Splunk data, extending investigations to SIEM-stored events
  - *Reference:* [Splunk Plugin for Security Copilot](https://learn.microsoft.com/en-us/copilot-security/splunk-plugin)

### Web Intelligence Use Cases

- **Open-source intelligence gathering** - Analysts need current industry information and threat landscape context without pre-configured integrations
  - *Solution:* Enable the public web plugin using anonymous authentication to access industry information from the public web directly within Copilot investigations

### Custom Development Use Cases

- **Proprietary security tool integration** - Organizations have internal security tools not supported by native plugins
  - *Solution:* Develop custom Copilot plugins using YAML or JSON manifest files to invoke specialized internal tools, with owner settings controlling who can add and manage these plugins
  - *Reference:* [Create Custom Plugins for Security Copilot](https://learn.microsoft.com/en-us/copilot-security/create-custom-plugins)

- **OpenAI API-based extensions** - Developers want to leverage OpenAI capabilities within Copilot workflows
  - *Solution:* Create custom plugins developed with OpenAI's API, requiring proper manifest files describing metadata and skill invocation methods

- **Controlled custom plugin deployment** - Organizations need governance over who can deploy custom plugins
  - *Solution:* Configure owner settings to restrict "Who can add and manage their own custom plugins" and "Who can add and manage custom plugins for everyone," ensuring contributor role permissions align with organizational policies

- **Plugin lifecycle management** - Custom plugins require ongoing maintenance and updates
  - *Solution:* Once added, custom plugins can be turned on or off, updated with new versions, or deleted as needed through the plugin management interface

---

## References

- [Manage Plugins in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/manage-plugins)
- [Create Custom Plugins for Security Copilot](https://learn.microsoft.com/en-us/copilot-security/create-custom-plugins)
- [ServiceNow Plugin for Security Copilot](https://learn.microsoft.com/en-us/copilot-security/servicenow-plugin)
- [Splunk Plugin for Security Copilot](https://learn.microsoft.com/en-us/copilot-security/splunk-plugin)
- [CrowdSec Threat Intelligence Plugin](https://learn.microsoft.com/en-us/copilot-security/crowdsec-plugin)
- [GreyNoise Plugin for Security Copilot](https://learn.microsoft.com/en-us/copilot-security/greynoise-plugin)
- [CIRCL Hash Lookup Plugin](https://learn.microsoft.com/en-us/copilot-security/circl-hash-plugin)
