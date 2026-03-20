# Copilot in Microsoft Purview

Microsoft Security Copilot is now accessible from within Microsoft Purview data security solutions, as part of the embedded experience. With Copilot in Microsoft Purview, data security and compliance admins can use the power of AI to assess risk exposure more quickly than is otherwise possible, directly from within Microsoft Purview solutions.

&gt; **Note:** The list of Copilot capabilities embedded in Microsoft Purview is continually growing. This unit provides just a sampling of those capabilities. For more information, see documentation on Microsoft Purview.

Some of the scenarios supported as part of the embedded experience include:

- Gain comprehensive summary of Data Loss Prevention alerts.
- Gain comprehensive summary of Insider Risk Management alerts.
- Gain contextual summary of Communication Compliance policy matches.
- Gain contextual summary of evidence collected in eDiscovery review sets.

For all use cases supported through the embedded experience, as is the case with the standalone experience, your organization must be onboarded to Security Copilot, the Purview plugin must be enabled in Copilot, and your organization must be licensed and onboarded to the applicable Microsoft Purview solutions. To enable the Microsoft Purview plugin, the option to allow Security Copilot to access data from your Microsoft 365 services must be enabled, as part of the owner plugin settings.

<img width="567" height="245" alt="image" src="https://github.com/user-attachments/assets/f5deb6b0-ba03-46a3-b9aa-a73f91d1496d" />

Additionally, users must have the appropriate role permissions for both Copilot and the Purview solutions. For Copilot, users need, at a minimum, the Copilot workspace contributor role or the Microsoft Entra Security operator role. For Microsoft Purview, as is true for a Microsoft solution enabled via a plugin, Copilot assumes the permissions of the user when it tries to access the data to answer the queries, so you need to have the required permissions to access the data.

---

## Gain Comprehensive Summary of Alerts

Data security teams generally receive more data security alerts per day than they can review, leaving them exposed to risks. To help with this challenge, Copilot in Microsoft Purview uses the power of generative AI to provide a summary for the alert you want to review and help accelerate your investigation. This capability is supported in Microsoft Purview Data Loss Prevention and Microsoft Purview Insider Risk Management.

### Data Loss Prevention

To summarize Data Loss Prevention alerts using Copilot:

1. Sign in to the Microsoft Purview compliance portal or the new Microsoft Purview portal and select the Data Loss Prevention solution.
2. Navigate to the alerts queue and select the alert you want to review.

  <img width="2507" height="1213" alt="image" src="https://github.com/user-attachments/assets/8360e7a7-a44c-4df1-9bbc-c19793356087" />

4. Select "Get a summary from Security Copilot."

From the alert summary, you can use the ellipses on the top right of the alert summary to copy the response to clipboard, regenerate, or transition to the standalone experience by selecting Open in Security Copilot.

<img width="537" height="417" alt="image" src="https://github.com/user-attachments/assets/822e8170-c2c5-4e54-ac52-a428b10fb68f" />

### Insider Risk Management

To summarize Insider Risk Management alerts using Copilot, you follow similar steps as described for DLP.

You sign in to the Microsoft Purview compliance portal or the new Microsoft Purview portal and go to the Insider Risk Management solution. Navigate to the alerts queue to select the alert you want to review. Information about the alert and the option to summarize the alert are displayed.

<img width="919" height="387" alt="image" src="https://github.com/user-attachments/assets/71a752ee-4033-41bf-9ab1-0534e82f1a1c" />

You select Summarize to have Copilot generate the alert summary. From the alert summary, you can use the ellipses on the top right of the alert summary to copy the response to clipboard, regenerate, or open it in the standalone Copilot experience.

<img width="372" height="560" alt="image" src="https://github.com/user-attachments/assets/5876ce18-a8a3-496b-8aa4-c7f2594456f1" />

The ability to summarize Insider Risk Management alerts, enables you to quickly gain the highlights of the potential incident by identifying critical user details like exfiltration activities, patterns, user roles, and unusual activities that may lead to potential security incidents.

---

## Gain Contextual Summary of Content in a Communication Compliance Policy

Reviewing communications is an integral part of protecting your organization's communication landscape, but it's also time-consuming to review content that is hundreds of words long or contain attachments. With Copilot, you can now:

- Get a contextual summary of a message and its attachments in the context of classifier conditions that flagged the message.
- Ask follow-up contextual questions about the message and its attachments.

Contextual Summarization currently supports trainable classifiers as context and contextual summaries are only eligible for messages and attachments with a combined length of 100 words or more.

Before you get started, ensure you have proper licensing to access Communication Compliance and the appropriate role permissions for Copilot and Communication Compliance. To get contextual summaries in policies, you must have Communication Compliance or Communication Compliance Investigator Role. For Copilot, you need, as a minimum, the Entra Security operator or Copilot workspace contributor role.

To get started:

1. Navigate to the Communication Compliance solution from the Microsoft Purview compliance portal or the new Microsoft Purview portal, then navigate to the Policies tab in Communication Compliance.
2. Navigate to a policy that uses trainable classifiers as part of the policy's configurations and select a policy match to view message content.
3. A Copilot action button appears in the upper left command bar or a Summarize action button in the lower right command bar. Select either action to generate a contextual summary of the message and supported attachments.

<img width="1080" height="539" alt="image" src="https://github.com/user-attachments/assets/32ef3bab-24e7-4703-8cd5-77c9f23d6654" />

To learn more about the message, explore other default prompts or type your own question into the text prompt in the Copilot side panel.

<img width="376" height="332" alt="image" src="https://github.com/user-attachments/assets/5b9d07ea-3275-4450-a46a-c4cf03bca04e" />

---

## Gain Contextual Summary of Evidence Collected in eDiscovery Review Sets

eDiscovery admins or managers spend a significant amount of time reviewing evidence collected in review sets. Copilot embedded with Microsoft Purview eDiscovery (Premium) can help you optimize your time. With Copilot, you can now:

- Get a contextual summary of a single item in a review set.
- Ask follow-up contextual questions about the summary.

To use Copilot in Microsoft Purview with eDiscovery (Premium), you must be licensed for eDiscovery (Premium) and have the appropriate role permissions for Copilot and for eDiscovery. You must have access to eDiscovery (Premium) cases, and to obtain a contextual summary for an item in a review set, the Purview Review role is required. For Copilot, you need, as a minimum, the Entra Security operator or Copilot workspace contributor role.

To get started:

1. Navigate to the Microsoft Purview compliance portal (this use case isn't currently supported in the new Microsoft Purview portal), then navigate to an eDiscovery (Premium) case.
2. Navigate to and open a review set.
3. Select an item from the review set that you want Copilot to summarize, then select Summarize. Contextual summary of an item is supported only for files types with text extraction support. Copilot only supports single-item summary.

You can ask more questions or select one of the default prompts to gain further insights into the generated summary.

<img width="1177" height="747" alt="image" src="https://github.com/user-attachments/assets/a93b83cf-8628-4d0c-845a-eda69eaa0c44" />

---

## Feedback

For any AI generated content, you can provide feedback and accuracy of the content. Select the feedback prompt on the bottom right of the content window and select from the available options: confirmed, it looks great, off target, inaccurate, or potentially harmful, inappropriate.

<img width="462" height="492" alt="image" src="https://github.com/user-attachments/assets/d6be545d-8794-4f9b-90c3-19a05f1d22e0" />

---

## Use Cases and Solutions

### Alert Management Use Cases

- **DLP alert overload** - Data security teams receive more alerts than they can manually review, creating exposure risk
  - *Solution:* Navigate to the DLP alerts queue in Microsoft Purview compliance/new portal, select the alert, and choose "Get a summary from Security Copilot" to get AI-generated summaries; use ellipses to copy, regenerate, or open in standalone experience
  - *Reference:* [Copilot in Microsoft Purview DLP](https://learn.microsoft.com/en-us/purview/dlp-copilot)

- **Insider risk investigation acceleration** - Security teams need to quickly understand potential insider threats from complex alert data
  - *Solution:* Access Insider Risk Management alerts queue, select Summarize to generate AI summaries highlighting exfiltration activities, patterns, user roles, and unusual activities; leverage the standalone experience for deeper investigation
  - *Reference:* [Copilot in Insider Risk Management](https://learn.microsoft.com/en-us/purview/insider-risk-management-copilot)

### Communication Compliance Use Cases

- **Lengthy communication review** - Compliance teams spend excessive time reviewing long messages and attachments for policy violations
  - *Solution:* Navigate to Communication Compliance policies using trainable classifiers, select policy matches with 100+ words, and use the Copilot action or Summarize button to get contextual summaries of messages and attachments; ask follow-up questions in the Copilot side panel
  - *Reference:* [Copilot in Communication Compliance](https://learn.microsoft.com/en-us/purview/communication-compliance-copilot)

### eDiscovery Use Cases

- **Evidence review optimization** - eDiscovery admins spend significant time reviewing individual items in large review sets
  - *Solution:* Access eDiscovery (Premium) cases in the Microsoft Purview compliance portal, open review sets, select single items with text extraction support, and choose Summarize for contextual summaries; ask follow-up questions or use default prompts for deeper insights
  - *Reference:* [Copilot in Microsoft Purview eDiscovery](https://learn.microsoft.com/en-us/purview/ediscovery-copilot)

### Enablement and Permissions Use Cases

- **Purview plugin activation** - Copilot features are unavailable in Purview despite proper licensing
  - *Solution:* Ensure organization is onboarded to Security Copilot, enable the Purview plugin in owner plugin settings, and specifically allow Security Copilot to access data from Microsoft 365 services; verify users have Copilot workspace contributor or Entra Security operator roles AND required Purview solution permissions
  - *Reference:* [Enable Microsoft Purview Plugin](https://learn.microsoft.com/en-us/copilot-security/manage-plugins)

- **Permission inheritance issues** - Copilot cannot access Purview data despite user having Purview access
  - *Solution:* Verify user has minimum Entra Security operator or Copilot workspace contributor role for Copilot access, plus specific Purview solution roles (e.g., Communication Compliance Investigator Role, Purview Review role for eDiscovery); remember Copilot assumes user permissions when accessing data

### Quality Assurance Use Cases

- **AI response validation** - Users need to verify accuracy of Copilot-generated summaries for compliance decisions
  - *Solution:* Use the feedback prompt on bottom right of any AI-generated content to mark as confirmed/looks great, off target, inaccurate, or potentially harmful/inappropriate, contributing to model improvement
  - *Reference:* [Provide Feedback in Security Copilot](https://learn.microsoft.com/en-us/copilot-security/provide-feedback)

---

## References

- [Microsoft Purview Documentation](https://learn.microsoft.com/en-us/purview/)
- [Copilot in Microsoft Purview](https://learn.microsoft.com/en-us/purview/copilot-in-purview)
- [Copilot in Microsoft Purview Data Loss Prevention](https://learn.microsoft.com/en-us/purview/dlp-copilot)
- [Copilot in Microsoft Purview Insider Risk Management](https://learn.microsoft.com/en-us/purview/insider-risk-management-copilot)
- [Copilot in Microsoft Purview Communication Compliance](https://learn.microsoft.com/en-us/purview/communication-compliance-copilot)
- [Copilot in Microsoft Purview eDiscovery](https://learn.microsoft.com/en-us/purview/ediscovery-copilot)
- [Manage Plugins in Security Copilot](https://learn.microsoft.com/en-us/copilot-security/manage-plugins)
- [Provide Feedback in Security Copilot](https://learn.microsoft.com/en-us/copilot-security/provide-feedback)
- [Microsoft Security Copilot Roles](https://learn.microsoft.com/en-us/copilot-security/assign-roles)
