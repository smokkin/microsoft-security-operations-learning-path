# Copilot in Microsoft Intune

Microsoft Intune has capabilities that are powered by Microsoft Security Copilot. These capabilities access your Intune data, and can help you manage your policies & settings, understand your security posture, and troubleshoot device issues.

Access to your Intune data is supported through Microsoft Security Copilot, referred to as the standalone experience, or embedded within the Intune admin center, referred to as Copilot in Intune. This unit focuses on the embedded experience.

> Note: The list of Copilot capabilities embedded in Microsoft Intune is continually growing. This unit provides just a sampling of those capabilities. For more information, see documentation on Microsoft Intune.

---

## Before You Begin

To enable Copilot to access your Intune data, for either the embedded or standalone experience, Microsoft Security Copilot must be configured, the Microsoft Intune plugin must be enabled, and you need to have appropriate role permissions. You need a role permission that grants access to Copilot and you also need a separate Intune service-specific role like the Intune Endpoint Security Manager role. There isn't a built-in Intune role that includes access to Copilot.

<img width="701" height="250" alt="image" src="https://github.com/user-attachments/assets/d2f625c1-93e9-4c9a-9f2b-785f0e88e0f6" />

For the specific setup tasks, go to Describe how to enable Microsoft Security Copilot.

You can check the status of Copilot in Intune from the Intune admin center.

<img width="1008" height="701" alt="image" src="https://github.com/user-attachments/assets/a48d43b5-6f39-46ff-a3ec-b41c1205e4c5" />

---

## Copilot in Intune

Currently, Copilot in Intune is available for:

- Policy and setting management
- Device details and troubleshooting

---

## Policy and Setting Management

Copilot is embedded on policy settings and with your existing policies, on the following policy types in Intune:

- Compliance policies
- Device configuration policies, including the settings catalog
- Most endpoint security policies

When you create a new policy, you can use Copilot to learn more about individual settings, their impact, and recommended values by using the Copilot tooltips.

The example that follows shows the compliance settings tab for a new macOS compliance policy. Next to each setting is a Copilot icon. Selecting the Copilot icon displays detailed information about the setting.

<img width="1055" height="805" alt="image" src="https://github.com/user-attachments/assets/c7eac90f-54e1-4565-a7cf-d92f24bdd32c" />

From an existing policy, you can use Copilot to summarize the policy. The summary describes what the policy does, the users and groups assigned to the policy, and the settings in the policy. This feature can help you understand the impact of a policy and its settings on your users and devices.

<img width="903" height="704" alt="image" src="https://github.com/user-attachments/assets/c8d217e0-8559-4672-8441-c758ad416661" />

Whether you're using Copilot to learn about the settings for a new policy or summarizing an existing policy, the Copilot window provides more prompts that you can use. You can also select the prompt guide icon on the bottom right and select from an existing list of prompts.

<img width="444" height="288" alt="image" src="https://github.com/user-attachments/assets/4d3f39d3-c4d3-4ac0-8b06-ec1b909975ac" />

---

## Device Details and Troubleshooting

You can use Copilot to get device-specific information, like the installed apps, group membership, and other information that can help troubleshoot a device.

<img width="1279" height="703" alt="image" src="https://github.com/user-attachments/assets/a1c6e731-8174-4530-8abc-dac786fe0cf6" />

When the Copilot window opens, select a prompt, and enter any required or optional input, if needed. You can also open the prompt guide for some follow-up questions.

---

## Use Cases and Solutions

### Policy Management Use Cases

- **New policy configuration guidance** - Administrators need to understand individual policy settings and their impact when creating new compliance or configuration policies
  - *Solution:* Use Copilot tooltips (Copilot icon next to each setting) when creating new policies to get detailed information about settings, their impact, and recommended values
  - *Reference:* [Copilot in Microsoft Intune](https://learn.microsoft.com/en-us/mem/intune/fundamentals/copilot-in-intune)

- **Existing policy impact assessment** - IT teams need to understand what existing policies do and their effects on users/devices
  - *Solution:* Use Copilot to summarize existing compliance policies, device configuration policies (including settings catalog), and endpoint security policies to see what the policy does, assigned users/groups, and configured settings

- **Policy troubleshooting preparation** - Administrators need follow-up questions to better understand policy configurations
  - *Solution:* Use the prompt guide icon in the Copilot window to select from existing lists of prompts for deeper policy analysis

### Device Management Use Cases

- **Device-specific troubleshooting** - Help desk teams need device context (installed apps, group membership) to resolve support tickets
  - *Solution:* Access Copilot in Intune for device details, select prompts for device-specific information, enter required input, and use the prompt guide for follow-up troubleshooting questions
  - *Reference:* [Troubleshoot Devices with Copilot in Intune](https://learn.microsoft.com/en-us/mem/intune/fundamentals/copilot-in-intune#device-details-and-troubleshooting)

### Enablement Use Cases

- **Intune plugin activation** - Copilot features are unavailable in Intune despite proper licensing
  - *Solution:* Configure Microsoft Security Copilot, enable the Microsoft Intune plugin, and ensure users have both Copilot access permissions AND an Intune service-specific role (e.g., Intune Endpoint Security Manager); note there is no built-in Intune role that includes Copilot access
  - *Reference:* [Enable Microsoft Intune Plugin](https://learn.microsoft.com/en-us/copilot-security/manage-plugins)

- **Status verification** - Administrators need to confirm Copilot in Intune is properly enabled
  - *Solution:* Check the status of Copilot in Intune from the Intune admin center to verify the embedded experience is active

---

## References

- [Microsoft Intune Documentation](https://learn.microsoft.com/en-us/mem/intune/)
- [Copilot in Microsoft Intune](https://learn.microsoft.com/en-us/mem/intune/fundamentals/copilot-in-intune)
- [Manage Plugins in Security Copilot](https://learn.microsoft.com/en-us/copilot-security/manage-plugins)
- [Intune Endpoint Security Manager Role](https://learn.microsoft.com/en-us/mem/intune/fundamentals/role-based-access-control)
- [Microsoft Security Copilot Setup](https://learn.microsoft.com/en-us/copilot-security/provision-capacity)
