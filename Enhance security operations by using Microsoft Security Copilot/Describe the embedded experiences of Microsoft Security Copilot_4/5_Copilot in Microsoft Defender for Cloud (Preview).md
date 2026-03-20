# Copilot in Microsoft Defender for Cloud (Preview)

Defender for Cloud integrates Copilot directly in to the Defender for Cloud experience. This integration allows you to analyze, summarize, remediate, and delegate your recommendations with natural language prompts

Copilot in Defender for Cloud is available for all users when you:

- Enable Defender for Cloud on your environment.
- Have access to Azure Copilot.
- Have Security Compute Units assigned for Security Copilot.

Copilot in Defender for Cloud isn't reliant on any of the available plans in Defender. However, in order to enjoy the full range of Copilot's capabilities in Defender for Cloud, we recommend enabling the Defender for Cloud Security Posture Management (DCSPM) plan on your environments. The DCSPM plan includes many extra security features such as Attack path analysis, Risk prioritization and more, all of which can be navigated and managed using Security Copilot. Without the DCSPM plan, you're still able to use Copilot in Defender for Cloud, but in a limited capacity.

> Note: The list of Copilot capabilities embedded in Microsoft Defender for Cloud is continually growing. This unit provides just a sampling of those capabilities. For more information, see documentation on Microsoft Defender for Cloud.

---

## Analyze Recommendations with Security Copilot

Microsoft Defender for Cloud's integration with Security Copilot allows you to analyze all of the recommendations presented on the recommendations page. By narrowing the scope of the recommendations page, you can focus on specific recommendations and get a better understanding of your security posture.

Once the list of recommendations is filtered, you can investigate specific recommendations and gain a better understanding of the risks and vulnerabilities that are present in your environment.

To analyze your recommendations:

1. From the Azure portal, search for and select Microsoft Defender for Cloud.
2. Navigate to Recommendations.
3. Select **Analyze with Copilot**.

   <img width="1872" height="958" alt="image" src="https://github.com/user-attachments/assets/d704da9d-3080-43a6-a072-e04c464a91bb" />

5. Select one of the suggested prompts or enter a prompt in natural language. Some sample prompts include:

- Show risks for publicly exposed resources
- Show risks for resources with sensitive data
- Show risks for critical resources

Copilot generates an initial analysis and you can filter the list of recommendation based on that initial analysis. You can further refine the results by selecting one of the suggested follow-up prompts or entering one manually, and applying the filter.

The recommendations page updates with the appropriate filters applied based on the prompts you provided. Copilot remains open and you can enter other prompts as needed.

<img width="377" height="815" alt="image" src="https://github.com/user-attachments/assets/94227181-8d16-49fd-93d0-97f20a58928d" />

---

## Summarize Recommendations with Security Copilot

Microsoft Defender for Cloud's integration with Security Copilot allows you to summarize a recommendation to get a better understanding of the risks and vulnerabilities that are present in your environment.

By summarizing a recommendation, you can get a quick overview of the recommendation in natural language. Summarizing the recommendation helps you understand the information presented in a recommendation and allows you to prioritize your remediation efforts.

Once a recommendation is selected, you can summarize it with Copilot. By using prompts, you can get a better understanding of the recommendation and decide how best to handle it.

To summarize a selected recommendation:

1. From the Azure portal, search for and select Microsoft Defender for Cloud.
2. Navigate to Recommendations, then select a recommendation.
3. From the recommendation page, select **Summarize with Copilot**.

   <img width="1872" height="958" alt="image" src="https://github.com/user-attachments/assets/fd721542-bdbe-4eaa-948d-9857a556bbff" />

5. Once Copilot generates a summary response, you enter more prompts as needed.

Once you have a better understanding of the recommendation, you can decide how best to handle it. You can, for example, select to have Copilot help you remediate the recommendation, delegate the remediation to the resource owner, or you can enter other prompts as needed.

---

## Remediate Recommendations with Security Copilot

Microsoft Defender for Cloud's integration with Security Copilot allows you to remediate recommendations that are present on the recommendations page with natural language prompts. Remediating a recommendation with Security Copilot allows you to improve your security posture by addressing the risks and vulnerabilities that are present in your environment.

Once a recommendation is summarized with Copilot in Defender for Cloud, you can decide how best to handle it. By using prompts, you can have Security Copilot assist you in the remediation process.

To use Copilot in Defender for Cloud to assist with the remediation process for recommendations:

1. Summarize a recommendation, as described in the section, 'Summarize recommendations with Security Copilot'
2. Select **Help me remediate this recommendation**.
3. Review the suggested remediation information and follow the instructions to remediate the recommendation. In some cases, a recommendation may include a script that can be run to apply the remediation.

<img width="433" height="415" alt="image" src="https://github.com/user-attachments/assets/7a279ac4-188b-4eba-adcd-e216fdf19640" />

---

## Delegate Recommendations with Security Copilot

Microsoft Defender for Cloud's integration with Security Copilot allows you to delegate recommendations that are present on the recommendations page with natural language prompts. Recommendations can be delegated to another person or team.

Delegating recommendations can improve your security posture by having the right people address the risks and vulnerabilities presented by the recommendations that are present in your environment.

To use Copilot to delegate recommendations and ensure the right person or team is handling the risks and vulnerabilities that are present in your environment:

1. Summarize a recommendation, as described in the section, 'Summarize recommendations with Security Copilot.'
2. Select **Delegate the remediation to the resource owner**.
3. Copilot summarizes an email that it drafts. You can then select to view and send the email.

   <img width="462" height="721" alt="image" src="https://github.com/user-attachments/assets/fc6ae261-ca53-4309-bea7-01770a8b86a9" />

5. Review the email and add recipients, and select **Send**.

<img width="1014" height="763" alt="image" src="https://github.com/user-attachments/assets/f35c51f0-9192-4733-beaa-7d3aedfac6e2" />

Once the recommendation is delegated, you can monitor the progress of the remediation on Defender for Cloud's recommendations page. Copilot remains open and you can enter other prompts as needed.

---

## Remediate Code with Security Copilot

Microsoft Defender for Cloud's integration with Security Copilot allows you to remediate Infrastructure as Code (IaC) misconfigurations that are discovered in your code repositories. Remediating an IaC finding with Copilot allows you to address security misconfigurations and vulnerabilities early in the development cycle by automatically generating Pull Requests (PRs) that correct the identified weaknesses. Remediating these misconfigurations and vulnerabilities ensure that security issues in code are addressed accurately and promptly.

To use Copilot to help remediate Infrastructure as Code (IaC) misconfigurations that are discovered in your code repositories, you must:

- Enable Defender for Cloud on your environment.
- Have access to Azure Copilot.
- Have Security Compute Units assigned for Security Copilot.
- Connect your Azure DevOps environment to Defender for Cloud.
- Configure the Microsoft Security DevOps Azure DevOps extension.
- Review and ensure you meet the DevOps security support and prerequisites requirements.

To remediate an Infrastructure as Code scanning finding:

1. From the Azure portal, search for and select Microsoft Defender for Cloud.
2. Navigate to Recommendations.
3. Search for recommendations with the title 'Azure DevOps repositories should have infrastructure as code scanning findings resolved' recommendation then select any of the resulting recommendations.
4. Select **Reduce risk with Copilot**.
   
   <img width="1099" height="932" alt="image" src="https://github.com/user-attachments/assets/79296405-0efc-4bc9-950b-6ab3ca5d2d10" />

6. By selecting 'Select security check,' Copilot can generate pull requests to remediate supported security checks from the recommendation.

5. Select the appropriate description followed by the select button.

   <img width="1010" height="776" alt="image" src="https://github.com/user-attachments/assets/c5bb5f11-9e9e-499e-b4e0-a2caf5b84076" />

7. Review the summary of the code fix, then select **Submit**.
8. Select the provided link.
9. Review the PR.

Once the PR is generated in your code repository, you should have a developer review and approve the PR to have it merged into the code base.

---

## Use Cases and Solutions

### Recommendation Analysis Use Cases

- **Overwhelming recommendation volume** - Security teams face too many Defender for Cloud recommendations to prioritize effectively
  - *Solution:* Navigate to Recommendations, select Analyze with Copilot, and use natural language prompts (e.g., "Show risks for publicly exposed resources") to filter and focus on specific recommendation categories; refine results with follow-up prompts
  - *Reference:* [Analyze Recommendations with Copilot in Defender for Cloud](https://learn.microsoft.com/en-us/azure/defender-for-cloud/copilot-in-defender-for-cloud#analyze-recommendations)

- **Risk-based prioritization** - Teams need to understand which recommendations pose the greatest risk to sensitive or critical resources
  - *Solution:* Use sample prompts like "Show risks for resources with sensitive data" or "Show risks for critical resources" to filter recommendations by risk context and prioritize remediation efforts

### Recommendation Understanding Use Cases

- **Complex recommendation interpretation** - Security posture data is difficult to interpret for remediation prioritization
  - *Solution:* Select any recommendation and choose Summarize with Copilot to get a natural language overview of risks and vulnerabilities, enabling better understanding and prioritization decisions
  - *Reference:* [Summarize Recommendations with Copilot](https://learn.microsoft.com/en-us/azure/defender-for-cloud/copilot-in-defender-for-cloud#summarize-recommendations)

### Remediation Execution Use Cases

- **Guided remediation execution** - Teams need step-by-step assistance to implement security recommendations
  - *Solution:* After summarizing a recommendation, select "Help me remediate this recommendation" to receive AI-assisted remediation guidance, including executable scripts where applicable
  - *Reference:* [Remediate Recommendations with Copilot](https://learn.microsoft.com/en-us/azure/defender-for-cloud/copilot-in-defender-for-cloud#remediate-recommendations)

- **Remediation delegation** - Security teams lack direct access to remediate certain resources and need to assign tasks to resource owners
  - *Solution:* Select "Delegate the remediation to the resource owner" from a summarized recommendation; review the AI-drafted email, add recipients, and send to assign remediation responsibility while monitoring progress on the recommendations page

### DevOps Security Use Cases

- **IaC misconfiguration remediation** - Infrastructure as Code contains security misconfigurations discovered in Azure DevOps repositories
  - *Solution:* Search for the "Azure DevOps repositories should have infrastructure as code scanning findings resolved" recommendation, select Reduce risk with Copilot, choose the appropriate security check, review the code fix summary, submit to generate a PR, and have developers review and approve the PR to merge fixes into the codebase
  - *Reference:* [Remediate Code with Copilot in Defender for Cloud](https://learn.microsoft.com/en-us/azure/defender-for-cloud/copilot-in-defender-for-cloud#remediate-code)

### Enablement and Capacity Use Cases

- **Limited Copilot functionality** - Copilot features in Defender for Cloud appear restricted despite proper setup
  - *Solution:* Enable the Defender for Cloud Security Posture Management (DCSPM) plan to access full Copilot capabilities including Attack path analysis and Risk prioritization; without DCSPM, Copilot operates in limited capacity
  - *Reference:* [Enable Defender for Cloud Plans](https://learn.microsoft.com/en-us/azure/defender-for-cloud/enable-enhanced-security)

- **Prerequisites verification** - IaC remediation features are unavailable in Copilot
  - *Solution:* Verify all requirements: Defender for Cloud enabled, Azure Copilot access, Security Compute Units assigned, Azure DevOps environment connected to Defender for Cloud, Microsoft Security DevOps Azure DevOps extension configured, and DevOps security prerequisites met

---

## References

- [Microsoft Defender for Cloud Documentation](https://learn.microsoft.com/en-us/azure/defender-for-cloud/)
- [Copilot in Microsoft Defender for Cloud](https://learn.microsoft.com/en-us/azure/defender-for-cloud/copilot-in-defender-for-cloud)
- [Analyze Recommendations with Security Copilot](https://learn.microsoft.com/en-us/azure/defender-for-cloud/copilot-in-defender-for-cloud#analyze-recommendations)
- [Summarize Recommendations with Security Copilot](https://learn.microsoft.com/en-us/azure/defender-for-cloud/copilot-in-defender-for-cloud#summarize-recommendations)
- [Remediate Recommendations with Security Copilot](https://learn.microsoft.com/en-us/azure/defender-for-cloud/copilot-in-defender-for-cloud#remediate-recommendations)
- [Remediate Code with Security Copilot](https://learn.microsoft.com/en-us/azure/defender-for-cloud/copilot-in-defender-for-cloud#remediate-code)
- [Enable Defender for Cloud Plans](https://learn.microsoft.com/en-us/azure/defender-for-cloud/enable-enhanced-security)
- [Connect Azure DevOps to Defender for Cloud](https://learn.microsoft.com/en-us/azure/defender-for-cloud/quickstart-onboard-devops)
- [Microsoft Security DevOps Extension](https://learn.microsoft.com/en-us/azure/defender-for-cloud/azure-devops-extension)
