# Copilot in Microsoft Entra

Identity risk investigation is a crucial step to defend an organization. Microsoft Entra ID Protection applies the capabilities of Microsoft Security Copilot to summarize a user's risk level, provide insights relevant to the incident at hand, and provide recommendations for rapid mitigation.

> Note: The list of Copilot capabilities embedded in Microsoft Entra is continually growing. This unit provides just a sampling of those capabilities. For more information, see documentation on Microsoft Entra.

Before you get started with Copilot in Microsoft Entra, your organization must be onboarded to Security Copilot, the Microsoft Entra plugin must be enabled in Copilot, and users must have the appropriate role permissions. Copilot assumes the permissions of the user when it tries to access the data to answer the queries, so you need to have the required permissions to access the Microsoft Entra data.

To view and investigate a user's risky sign-ins:

1. Sign in to the Microsoft Entra admin.
2. Navigate to Protection &gt; Identity Protection and then to the Risky users report.
   
   <img width="1028" height="541" alt="image" src="https://github.com/user-attachments/assets/838e8f79-4fff-4408-91e9-002fe8c44eb2" />
   
4. Select a user from the risky users report.
5. Select the **Summarize** tab in the Risky User Details window.

<img width="614" height="691" alt="image" src="https://github.com/user-attachments/assets/d0d823c8-6fbb-4e74-8569-07388f0d459b" />

The risky user summary contains three sections:

- **Summary by Copilot:** summarizes in natural language why the user risk level was elevated.
- **What to do:** lists actionable insights tailored to the incident at hand to resolve the risk.
- **Help and documentation:** lists customized recommendation for how to mitigate against those types of attacks, with quick links to help and documentation.

Users can provide feedback on the generated content.

<img width="986" height="318" alt="image" src="https://github.com/user-attachments/assets/59eb05a0-826b-45da-8e84-fedaa1fef1ef" />

---

## Use Cases and Solutions

### Identity Risk Investigation Use Cases

- **Rapid risk assessment** - Security teams need to quickly understand why a user's risk level was elevated without manually reviewing multiple data sources
  - *Solution:* Navigate to Identity Protection &gt; Risky users report, select the user, and open the Summarize tab to get a Copilot-generated natural language summary explaining the risk elevation, actionable mitigation steps, and customized documentation links
  - *Reference:* [Copilot in Microsoft Entra ID Protection](https://learn.microsoft.com/en-us/entra/id-protection/copilot-in-entra-id-protection)

- **Incident-tailored response** - Identity risks require specific remediation actions based on the attack type
  - *Solution:* Review the "What to do" section in the risky user summary for actionable insights tailored to the specific incident, enabling rapid risk resolution

- **Knowledge gap mitigation** - Analysts encounter unfamiliar attack types during identity investigations
  - *Solution:* Use the "Help and documentation" section which provides customized recommendations and quick links to relevant mitigation guidance for the specific attack types encountered

### Enablement Use Cases

- **Entra plugin activation** - Copilot features are unavailable in Entra ID Protection despite proper licensing
  - *Solution:* Ensure organization is onboarded to Security Copilot and the Microsoft Entra plugin is enabled in Copilot settings; verify users have appropriate Microsoft Entra permissions as Copilot assumes user permissions when accessing data
  - *Reference:* [Enable Microsoft Entra Plugin](https://learn.microsoft.com/en-us/copilot-security/manage-plugins)

- **Permission-based access issues** - Copilot cannot retrieve Entra data for certain users
  - *Solution:* Verify users have the required Microsoft Entra permissions to access Identity Protection data, as Copilot operates under the user's existing permissions and cannot access data the user themselves cannot view

### Quality Assurance Use Cases

- **AI summary validation** - Security teams need to verify accuracy of Copilot-generated risk assessments
  - *Solution:* Use the feedback menu on generated content to mark responses as confirmed/looks great, off target, inaccurate, or potentially harmful/inappropriate, contributing to model improvement
  - *Reference:* [Provide Feedback in Security Copilot](https://learn.microsoft.com/en-us/copilot-security/provide-feedback)

---

## References

- [Microsoft Entra ID Protection Documentation](https://learn.microsoft.com/en-us/entra/id-protection/)
- [Copilot in Microsoft Entra ID Protection](https://learn.microsoft.com/en-us/entra/id-protection/copilot-in-entra-id-protection)
- [Manage Plugins in Security Copilot](https://learn.microsoft.com/en-us/copilot-security/manage-plugins)
- [Provide Feedback in Security Copilot](https://learn.microsoft.com/en-us/copilot-security/provide-feedback)
- [Microsoft Entra Roles and Permissions](https://learn.microsoft.com/en-us/entra/fundamentals/users-assign-role-azure-portal)
