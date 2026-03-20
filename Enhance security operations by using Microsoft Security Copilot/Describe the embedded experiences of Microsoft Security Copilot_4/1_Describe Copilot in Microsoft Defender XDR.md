# Describe Copilot in Microsoft Defender XDR

Microsoft Security Copilot is embedded in Microsoft Defender XDR to enable security teams to quickly and efficiently investigate and respond to incidents.

---

## Security Copilot Capabilities Embedded in Microsoft Defender XDR

Security Copilot capabilities embedded in Microsoft Defender XDR include:

- Summarize incidents
- Guided responses
- Script analysis
- Natural language to KQL queries
- Incident reports
- Analyze files
- Device summary

> Note: The list of Copilot capabilities embedded in Microsoft Defender XDR is continually growing. This unit provides just a sampling of some of those Copilot capabilities. For more information, see documentation on Microsoft Defender XDR.

There are also some options that are common across all these features, including the ability to provide feedback on prompt responses and seamlessly moving to the standalone experience.

As described in the introduction unit, in the embedded experience Copilot is able to invoke the product specific capabilities directly, providing processing efficiency. That said, to ensure access to these Microsoft Security Copilot features, the Microsoft Defender XDR plugin needs to be enabled and this is done through the standalone experience. To learn more, refer to Describe the features available in the standalone experience of Microsoft Security Copilot.

<img width="550" height="434" alt="image" src="https://github.com/user-attachments/assets/ee9424e2-9443-44c2-8b5a-c4636983fbf0" />

---

## Summarize Incidents

To immediately understand an incident, you can use Microsoft Copilot in Microsoft Defender XDR to summarize an incident for you. Copilot creates an overview of the attack containing essential information for you to understand what transpired in the attack, what assets are involved, and the timeline of the attack. Copilot automatically creates a summary when you navigate to an incident's page.

<img width="960" height="562" alt="image" src="https://github.com/user-attachments/assets/1551ca07-8b87-4257-9799-36d32f0f866e" />

Incidents containing up to 100 alerts can be summarized into one incident summary. An incident summary, depending on the availability of the data, includes the following:

- The time and date when an attack started.
- The entity or asset where the attack started.
- A summary of timelines of how the attack unfolded.
- The assets involved in the attack.
- Indicators of compromise (IOCs).
- Names of threat actors involved.

---

## Guided Responses

Copilot in Microsoft Defender XDR uses AI and machine learning capabilities to contextualize an incident and learn from previous investigations to generate appropriate response actions, which are shown as guided responses. The guided response capability of Copilot allows incident response teams at all levels to confidently and quickly apply response actions to resolve incidents with ease.

Guided responses recommend actions in the following categories:

- **Triage** - includes a recommendation to classify incidents as informational, true positive, or false positive
- **Containment** - includes recommended actions to contain an incident
- **Investigation** - includes recommended actions for further investigation
- **Remediation** - includes recommended response actions to apply to specific entities involved in an incident

Each card contains information about the recommended action, including why the action is recommended, similar incidents, and more. For example, the View similar incidents action becomes available when there are other incidents within the organization that are similar to the current incident. Incident response teams can also view user information for remediation actions such as resetting passwords.

<img width="293" height="555" alt="image" src="https://github.com/user-attachments/assets/bba772af-ae34-43f2-a78b-49c4031a0826" />

Not all incidents/alerts provide guided responses. Guided responses are available for incident types such as phishing, business email compromise, and ransomware.

---

## Analyze Scripts and Codes

Most complex and sophisticated attacks like ransomware evade detection through numerous ways, including the use of scripts and PowerShell. Moreover, these scripts are often obfuscated, which adds to the complexity of detection and analysis. Security operations teams need to quickly analyze scripts and code to understand its capabilities and apply appropriate mitigation to attacks from progressing further within a network.

The script analysis capability of Copilot in Microsoft Defender XDR provides security teams added capacity to inspect scripts and code without using external tools. This capability also reduces complexity of analysis, minimizing challenges and allowing security teams to quickly assess and identify a script as malicious or benign.

You can access the script analysis capability in the alert timeline within an incident, for a timeline entry consisting of script or code. In the image that follows, the timeline shows a powershell.exe entry.

> Note: Script analysis functions are continuously in development. Analysis of scripts in languages other than PowerShell, batch, and bash are being evaluated.

<img width="1211" height="757" alt="image" src="https://github.com/user-attachments/assets/76c73806-fed1-4087-bc8f-da88ce287d92" />

Copilot analyzes the script and displays the results in the script analysis card. Users can select the Show code to see specific lines of code related to the analysis. To hide the code, users need only to select Hide code.

<img width="342" height="431" alt="image" src="https://github.com/user-attachments/assets/e80f5ede-45cc-4002-8bd8-7d92a0e2906a" />

---

## Generate KQL Queries

Copilot in Microsoft Defender XDR comes with a query assistant capability in advanced hunting.

Threat hunters or security analysts who aren't yet familiar with or have yet to learn KQL can make a request or ask a question in natural language (for instance, Get all alerts involving user admin123). Copilot then generates a KQL query that corresponds to the request using the advanced hunting data schema.

This feature reduces the time it takes to write a hunting query from scratch so that threat hunters and security analysts can focus on hunting and investigating threats.

To access the natural language to KQL query assistant, users with access to Copilot select advanced hunting from the left navigation pane of the Defender XDR portal.

<img width="1333" height="524" alt="image" src="https://github.com/user-attachments/assets/fd339c65-c906-4f53-b727-b2f8a95ee17f" />

Using the prompt bar, the user can ask for a threat hunting query, using natural language, such as, "Give me all the devices that signed in within the last 10 minutes."

<img width="406" height="554" alt="image" src="https://github.com/user-attachments/assets/7e3dd0cc-e31c-43a3-9c87-c203ecf3981b" />

The user can then choose to run the query by selecting Add and run. The generated query then appears as the last query in the query editor. To make further tweaks, select Add to editor.

The option to run the generated query can also be set automatically through the settings icon.

<img width="402" height="104" alt="image" src="https://github.com/user-attachments/assets/ba53bb7e-2797-49a5-8ea1-c7f72d011a5f" />

---

## Create Incident Reports

A comprehensive and clear incident report is an essential reference for security teams and security operations management. However, writing a comprehensive report with the important details present can be a time-consuming task for security operations teams as it involves collecting, organizing, and summarizing incident information from multiple sources. Security teams can now instantly create an extensive incident report within the portal.

Utilizing Copilot's AI-powered data processing, security teams can immediately create incident reports with a click of a button in Microsoft Defender XDR.

While an incident summary provides an overview of an incident and how it happened, an incident report consolidates incident information from various data sources available in Microsoft Sentinel and Microsoft Defender XDR. The incident report also includes all analyst-driven steps and automated actions, the analysts involved in the response, and the comments from the analysts.

Copilot creates an incident report containing the following information:

- The main incident management actions' timestamps, including:
  - Incident creation and closure
  - First and last logs, whether the log was analyst-driven or automated, captured in the incident
- The analysts involved in incident response.
- Incident classification, including analysts' comments on how the incident was evaluated and classified.
- Investigation actions applied by analysts and noted in the incident logs
- Remediation actions done, including:
  - Manual actions applied by analysts and noted in the incident logs
  - Automated actions applied by the system, including Microsoft Sentinel Playbooks ran and Microsoft Defender XDR actions applied
- Follow up actions like recommendations, open issues, or next steps noted by the analysts in the incident logs.

To create an incident report, the user selects Generate incident report on the top right corner of the incident page or the icon in the Copilot pane.

<img width="700" height="409" alt="image" src="https://github.com/user-attachments/assets/3951c275-2b23-45d3-ac1a-542bfb6ddff6" />

The generated report depends on the incident information available from Microsoft Defender XDR and Microsoft Sentinel. By selecting the ellipses on the incident report card, the user can copy the report to the clipboard, post to an activity log, regenerate the report, or opt to open in the Copilot standalone experience.

<img width="313" height="521" alt="image" src="https://github.com/user-attachments/assets/be732c74-3834-41ec-ace5-2eef5e61a928" />

---

## Analyze Files

Sophisticated attacks often use files that mimic legitimate or system files to avoid detection. Copilot in Microsoft Defender XDR enables security teams to quickly identify malicious and suspicious files through AI-powered file analysis capabilities.

There are many ways to access the detailed profile page of a specific file. For example, you can use the search feature, you can select files from the evidence and response tab of an incident, or use the Incident graph.

In this example, you navigate to files through the incident graph of an incident with impacted files. The incident graph shows the full scope of the attack, how the attack spread through your network over time, where it started, and how far the attacker went.

From the incident graph, selecting files displays the option to view files. Selecting view files opens a panel on the right side of the screen listing impacted files. Selecting any file displays an overview of the file details and the option to analyze the file. Selecting Analyze opens the Copilot file analysis.

> Select file to analyze
<img width="1584" height="905" alt="image" src="https://github.com/user-attachments/assets/29d15f45-5d6e-4af3-b873-dfa2656ac397" />

> File analysis
<img width="759" height="486" alt="image" src="https://github.com/user-attachments/assets/43d4d6f1-8885-4976-a6de-f20e32e77684" />

---

## Summarize Devices and Identities

The device summary capability of Copilot in Defender enables security teams to get a device's security posture, vulnerable software information, and any unusual behaviors. Security analysts can use a device's summary to speed up their investigation of incidents and alerts.

There are many ways to access a device summary. In this example, you navigate to the device summary through the incident assets page. Selecting the assets tab for an incident displays all the assets. From the left navigation panel, select Devices then select a specific device name. From the overview page that opens on the right is the option to select Copilot.

Similarly, Copilot in Microsoft Defender XDR can summarize identities.

> Device summary
<img width="1912" height="956" alt="image" src="https://github.com/user-attachments/assets/70f06b8b-cbb4-4632-84ab-17edc62f6653" />

> Identity summary
<img width="1912" height="956" alt="image" src="https://github.com/user-attachments/assets/c8cf45db-7ca5-4358-988f-e5c4ea018553" />

---

## Common Functionality Across Key Features

There are some options that are common across the features of Copilot for Microsoft Defender XDR.

### Providing Feedback

As with the standalone experience, the embedded experience provides users a mechanism to provide feedback on the accuracy of the AI generated response. For any AI generated content, you can select the feedback prompt on the bottom right of the content window and select from the available options.

<img width="450" height="373" alt="image" src="https://github.com/user-attachments/assets/ba1d4035-1062-4fe8-a554-0f8305a022db" />

### Move to the Standalone Experience

As an analyst using Microsoft Defender XDR, you're likely to spend a good amount time in Defender XDR, so the embedded experience is a great place to start a security investigation. Depending on what you learn you may determine that a deeper investigation is needed. In this scenario, you can easily transition to the standalone experience to pursue a more detailed, cross product investigation that brings to bear all the Copilot capabilities enabled for your role.

For content generated through the embedded experience you can easily transition to the standalone experience. To move to the standalone experience, select the ellipses within the generated content window then choose Open in Security Copilot.

<img width="369" height="260" alt="image" src="https://github.com/user-attachments/assets/bd21da04-76e6-426a-9893-b019e0dfb31b" />

---

## Use Cases and Solutions

### Incident Response Use Cases

- **Rapid incident triage** - SOC analysts need immediate understanding of complex incidents with multiple alerts
  - *Solution:* Navigate to any incident page where Copilot automatically generates a summary (up to 100 alerts) containing attack timeline, involved assets, IOCs, and threat actor names, eliminating manual alert correlation
  - *Reference:* [Summarize Incidents with Copilot in Defender XDR](https://learn.microsoft.com/en-us/defender-xdr/security-copilot-in-microsoft-365-defender#summarize-incidents)

- **Consistent response execution** - Incident response teams need guidance on appropriate actions for specific incident types
  - *Solution:* Use Guided responses for phishing, business email compromise, and ransomware incidents to get AI-recommended actions across triage, containment, investigation, and remediation categories, with explanations and similar incident references
  - *Reference:* [Guided Responses in Microsoft Defender XDR](https://learn.microsoft.com/en-us/defender-xdr/security-copilot-in-microsoft-365-defender#guided-responses)

### Threat Hunting Use Cases

- **KQL skill gaps** - Threat hunters need to query Defender XDR data but lack KQL proficiency
  - *Solution:* Access the natural language to KQL query assistant from Advanced hunting, enter requests in plain English (e.g., "Give me all the devices that signed in within the last 10 minutes"), then add and run the generated query or add to editor for tweaks
  - *Reference:* [Natural Language to KQL in Defender XDR](https://learn.microsoft.com/en-us/defender-xdr/security-copilot-in-microsoft-365-defender#generate-kql-queries)

- **Obfuscated script analysis** - Analysts encounter suspicious PowerShell or batch scripts during investigations
  - *Solution:* Access script analysis from the alert timeline within an incident, select script/code entries (e.g., powershell.exe) to analyze without external tools, then show/hide specific code lines related to the AI-generated analysis
  - *Reference:* [Script Analysis in Microsoft Defender XDR](https://learn.microsoft.com/en-us/defender-xdr/security-copilot-in-microsoft-365-defender#analyze-scripts-and-codes)

### Investigation Use Cases

- **Malicious file identification** - Suspicious files mimicking legitimate system files require rapid analysis
  - *Solution:* Navigate to files via incident graph, evidence and response tab, or search; select any impacted file and choose Analyze to open Copilot file analysis for AI-powered malicious/suspicious file identification
  - *Reference:* [Analyze Files with Copilot in Defender XDR](https://learn.microsoft.com/en-us/defender-xdr/security-copilot-in-microsoft-365-defender#analyze-files)

- **Device security posture assessment** - Analysts need device context during incident investigation
  - *Solution:* Access device summaries through incident assets page (Assets tab &gt; Devices &gt; specific device &gt; Copilot) to get security posture, vulnerable software information, and unusual behaviors; use identity summaries for user context
  - *Reference:* [Device and Identity Summaries in Defender XDR](https://learn.microsoft.com/en-us/defender-xdr/security-copilot-in-microsoft-365-defender#summarize-devices-and-identities)

### Reporting Use Cases

- **Comprehensive incident documentation** - Security operations management requires detailed incident reports for compliance and review
  - *Solution:* Select Generate incident report from the incident page top right or Copilot pane to create reports consolidating timestamps, analyst actions, classifications, investigation/remediation steps, and follow-up actions from both Defender XDR and Sentinel; copy to clipboard, post to activity log, or regenerate as needed
  - *Reference:* [Create Incident Reports in Microsoft Defender XDR](https://learn.microsoft.com/en-us/defender-xdr/security-copilot-in-microsoft-365-defender#create-incident-reports)

### Workflow Integration Use Cases

- **Cross-product deep investigation** - Embedded analysis reveals need for broader cross-product investigation
  - *Solution:* Select ellipses within any AI-generated content window and choose Open in Security Copilot to seamlessly transition to standalone experience for detailed, cross-product investigations using all enabled Copilot capabilities
  - *Reference:* [Microsoft Security Copilot Standalone Experience](https://learn.microsoft.com/en-us/copilot-security/standalone-experience)

- **AI response quality improvement** - Users need to provide feedback on Copilot-generated content accuracy
  - *Solution:* Select feedback prompt on bottom right of any AI-generated content window to submit responses categorized as confirmed/looks great, off target, inaccurate, or potentially harmful/inappropriate
  - *Reference:* [Provide Feedback in Security Copilot](https://learn.microsoft.com/en-us/copilot-security/provide-feedback)

### Enablement Use Cases

- **Plugin activation requirements** - Defender XDR Copilot features are inaccessible despite proper licensing
  - *Solution:* Enable the Microsoft Defender XDR plugin through the standalone experience (Manage plugins window) to ensure embedded experience features are available; verify plugin status in standalone settings
  - *Reference:* [Enable Microsoft Defender XDR Plugin](https://learn.microsoft.com/en-us/copilot-security/manage-plugins)

---

## References

- [Microsoft Defender XDR Documentation](https://learn.microsoft.com/en-us/defender-xdr/)
- [Copilot in Microsoft Defender XDR](https://learn.microsoft.com/en-us/defender-xdr/security-copilot-in-microsoft-365-defender)
- [Summarize Incidents](https://learn.microsoft.com/en-us/defender-xdr/security-copilot-in-microsoft-365-defender#summarize-incidents)
- [Guided Responses](https://learn.microsoft.com/en-us/defender-xdr/security-copilot-in-microsoft-365-defender#guided-responses)
- [Analyze Scripts and Codes](https://learn.microsoft.com/en-us/defender-xdr/security-copilot-in-microsoft-365-defender#analyze-scripts-and-codes)
- [Generate KQL Queries](https://learn.microsoft.com/en-us/defender-xdr/security-copilot-in-microsoft-365-defender#generate-kql-queries)
- [Create Incident Reports](https://learn.microsoft.com/en-us/defender-xdr/security-copilot-in-microsoft-365-defender#create-incident-reports)
- [Analyze Files](https://learn.microsoft.com/en-us/defender-xdr/security-copilot-in-microsoft-365-defender#analyze-files)
- [Summarize Devices and Identities](https://learn.microsoft.com/en-us/defender-xdr/security-copilot-in-microsoft-365-defender#summarize-devices-and-identities)
- [Microsoft Security Copilot Standalone Experience](https://learn.microsoft.com/en-us/copilot-security/standalone-experience)
- [Manage Plugins in Security Copilot](https://learn.microsoft.com/en-us/copilot-security/manage-plugins)
- [Provide Feedback in Security Copilot](https://learn.microsoft.com/en-us/copilot-security/provide-feedback)
