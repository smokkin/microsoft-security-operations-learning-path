# Describe the Features Available in a Session of the Standalone Experience

A session is a particular conversation within Copilot and consists of one or more prompts. A session may be initiated through prompts you enter directly in the prompt bar, by running a promptbook, or a prompt suggestion.

Copilot has features that are common across all sessions and the individual prompts that make up a session, including:

- The process log
- Actions you can take a prompt and its response
- Prompt feedback
- The pin board

---

## Process Log

For every prompt Copilot runs, Copilot generates a process log that is visible to the user. The user can see what capability is used to generate the response. This is important because it enables the user to determine whether the response was generated from a trusted source. In the screenshot that follows, the process log shows that Copilot chose the Incident Analysis capability. The process log also shows that the final output went through safety checks, which is part of Microsoft's commitment to responsible AI.

<img width="736" height="472" alt="image" src="https://github.com/user-attachments/assets/90da3f86-dbca-424b-8f50-5326903fea12" />

---

## Action You Can Take on Prompt and Its Response

There's a consistent set of actions available for every prompt/response pair in the Copilot standalone experience. Actions include:

- Pin an individual prompt and its corresponding response to the pin board by selecting the pin icon.
- Edit a prompt.
- Rerun a prompt.
- Delete a prompt.
- Export a prompt.
- Copy a response.
- Provide feedback on a response

<img width="932" height="484" alt="image" src="https://github.com/user-attachments/assets/48f49617-a5e3-46ca-b898-07e29e284472" />

---

## Feedback

Whether you use promptbooks, prompt suggestions, or your own prompt, providing feedback about your satisfaction with the generated response can help Microsoft in improving Copilot. You can find the feedback buttons on the left-hand side at the bottom of every response.

You can select:

- Looks right
- Needs improvement
- Inappropriate

<img width="220" height="188" alt="image" src="https://github.com/user-attachments/assets/13f97192-1a15-4c63-81e2-6a451c25d43b" />

For each option, the user is prompted for additional information. The image that follows shows the options for a response that needs improvement.

The option to provide feedback is also available for Copilot features that are available in the embedded experience. Refer to Describe the embedded experiences of Microsoft Security Copilot.

<img width="220" height="188" alt="image" src="https://github.com/user-attachments/assets/3e1f4389-91e2-4e0a-9988-003ec99700f8" />

---

## Pin Board

The pin board enables you to keep track of important responses in a session. You can pin individual or multiple prompt-response pairs. To select one or more individual items, select the check box next to the item then select the pin icon. To select all the prompt-response pairs in the session, select the checkbox at the top of the session window then select the pin icon. Upon selecting the pin icon, the pin board window opens in a split view with the session. The pin board includes a summary tab that summarizes the session and a pinned items tab that lists the prompt and a collapsed view of the response that users can expand. You can also edit the title of the session on the pin board.

<img width="939" height="558" alt="image" src="https://github.com/user-attachments/assets/90babbd3-09ec-45f7-8876-500f152b2c74" />

The contents of the pin board can be shared so that people in your organization with Copilot access can view this session. Additionally, the contents of the pin board can be exported to Microsoft Word, sent via email, or copied.

<img width="452" height="249" alt="image" src="https://github.com/user-attachments/assets/f2d50d96-650a-4ef9-ad85-c23fe92ed523" />

<img width="583" height="217" alt="image" src="https://github.com/user-attachments/assets/e19ea4eb-20ed-4b48-bd7c-b477c48e8108" />

---

## Use Cases and Solutions

### Process Log Use Cases

- **Verifying response trustworthiness** - Security analysts need to validate that AI-generated responses come from reliable capabilities
  - *Solution:* Review the visible process log for each prompt to see which specific capability was used (e.g., Incident Analysis) and confirm the output passed safety checks, ensuring responsible AI compliance
  - *Reference:* [Microsoft Security Copilot Responsible AI](https://learn.microsoft.com/en-us/copilot-security/responsible-ai)

### Prompt Action Use Cases

- **Iterative prompt refinement** - Initial prompts don't produce the desired output and need adjustment
  - *Solution:* Use the Edit action to modify the original prompt, then Rerun to generate an improved response without retyping the entire query

- **Session cleanup and organization** - Sessions contain irrelevant or erroneous prompts that clutter the investigation
  - *Solution:* Delete individual prompt-response pairs to maintain clean, focused session histories

- **Response reuse across tools** - Analysts need to incorporate Copilot responses into other documents or communications
  - *Solution:* Copy responses directly for immediate use, or Export prompts for documentation and audit purposes

### Feedback Use Cases

- **Continuous model improvement** - Organizations want to contribute to Copilot accuracy improvements
  - *Solution:* Provide structured feedback using the "Looks right," "Needs improvement," or "Inappropriate" buttons, with additional details for "Needs improvement" to help Microsoft refine model performance
  - *Reference:* [Provide Feedback in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/provide-feedback)

- **Quality assurance reporting** - Security teams need to flag incorrect or problematic AI outputs
  - *Solution:* Mark responses as "Inappropriate" or "Needs improvement" to alert Microsoft to potential issues and contribute to safer AI outputs

### Pin Board Use Cases

- **Complex investigation tracking** - Multi-step security investigations generate multiple important findings that need organization
  - *Solution:* Pin individual or multiple prompt-response pairs (using checkboxes) to the pin board, which opens in split view with a summary tab and collapsible pinned items for quick reference

- **Cross-team collaboration** - Investigation findings need to be shared with team members who have Copilot access
  - *Solution:* Share the pin board contents directly with organization members, or export to Microsoft Word, send via email, or copy for distribution through other channels

- **Session documentation** - Investigations require formal documentation for compliance or management reporting
  - *Solution:* Export pin board contents to Microsoft Word for formal reporting, or use the summary tab to generate session overviews with editable titles

- **Efficient bulk selection** - Sessions contain numerous prompts requiring bulk actions
  - *Solution:* Use the top checkbox to select all prompt-response pairs in the session, then pin them collectively rather than individually

---

## References

- [Microsoft Security Copilot Documentation](https://learn.microsoft.com/en-us/copilot/security/)
- [Work with Sessions in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/work-with-sessions)
- [Provide Feedback in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/provide-feedback)
- [Microsoft Security Copilot Responsible AI](https://learn.microsoft.com/en-us/copilot-security/responsible-ai)
- [Describe Embedded Experiences](https://learn.microsoft.com/en-us/copilot-security/describe-embedded-experiences)
