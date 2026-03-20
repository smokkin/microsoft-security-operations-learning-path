# Describe Custom Promptbooks

Promptbooks in Security Copilot are collections of prompts put together to accomplish specific security-related tasks. They run one prompt after another, building on previous responses.

You can create your own promptbook with the promptbook builder to automate investigation flows and optimize repetitive steps in Copilot that are customized to your needs and requirements. You can also share the promptbooks you created with other users so they can also benefit from your work.

---

## Create a Promptbook from an Existing Session

To create your own promptbook, you can start with an existing session that contains the prompts you want to work with. For this example, the session titled, "Show the last three failed login attempts," is used.

<img width="912" height="332" alt="image" src="https://github.com/user-attachments/assets/e0025e67-297d-402a-a0d1-70f0ae3b8154" />

After selecting the desired session, select the boxes beside the prompts to include them or select the top box to include all prompts in the session. Selecting any or all of the prompts light up the Create promptbook button.

<img width="930" height="264" alt="image" src="https://github.com/user-attachments/assets/2f9876d7-3856-45bb-a7f8-fbf9c621e484" />

Once you select the create promptbook icon, the Create a promptbook page opens. Here you name the promptbook, add a tag and a description, add more prompts, and remove or edit existing prompts. If any of the prompts require an input parameter, you would need to specify an easily understood parameter name within angle brackets and no spaces. For example, if one of the prompts requires an incident ID number, you can specify `&lt;IncidentID&gt;`. Similarly, if a prompt requires that you enter a threat actor name, you could specify the input parameter as `&lt;threatactorname&gt;` or `&lt;ThreatActor&gt;`. You can include more than one input parameter. You can also select to share the promptbook with others in your organization or have it for your own personal use.

In the screenshot that follows, the promptbook is named Failed-Login-Attempts and it includes two prompts. The first prompt was originally to show the last three failed logins. To configure the number as an input parameter, select the ellipses next to the prompt to edit it by replacing the number 3 and entering `&lt;number&gt;`.

<img width="438" height="764" alt="image" src="https://github.com/user-attachments/assets/e75c651f-cc9a-42f8-a902-3f3c94e8f9d5" />

A pop-up window appears once your promptbook is created. From this window, you can select to view the promptbook you just created and then run it or edit it, share your promptbook via link, or go to the promptbook library.

<img width="474" height="238" alt="image" src="https://github.com/user-attachments/assets/c052318e-2486-482b-9465-96d6e268e72d" />

From then on, you can run your promptbook like you would any other promptbook. You can select the prompts icon from the prompt bar and start typing in the name of the promptbook in the search bar then selecting it from the list that appears.

<img width="533" height="220" alt="image" src="https://github.com/user-attachments/assets/52a2fbcb-e5e3-4da9-957d-04ff745378c0" />

Selecting the promptbook opens it. From here, you enter the required input parameter and then select run.

<img width="578" height="418" alt="image" src="https://github.com/user-attachments/assets/2ca6a32e-72ff-4095-9a43-d635bfe35118" />


---

## Edit a Promptbook

To edit your existing promptbook, select the home menu (hamburger icon) and select Promptbook library.

<img width="682" height="588" alt="image" src="https://github.com/user-attachments/assets/afc23f0a-1001-486a-9adc-c4aac8e6fa09" />

Select the ellipses for the promptbook you want to edit then select Edit from the options. You can only edit existing promptbooks if you're the owner of the promptbook.

<img width="917" height="490" alt="image" src="https://github.com/user-attachments/assets/dafd331a-ec7e-4ad5-8791-a0f56ea738b6" />

In addition to editing, you can also choose to view the details of the promptbook, duplicate it, or delete it. You can also choose to run the promptbook by selecting the Get started button.

---

## Use Cases and Solutions

### Investigation Automation Use Cases

- **Repetitive security investigation workflows** - Security analysts perform the same multi-step investigations frequently (e.g., failed login analysis)
  - *Solution:* Create a custom promptbook from an existing session by selecting relevant prompts, parameterizing variables (e.g., replacing "3" with `&lt;number&gt;`), and running the promptbook with input parameters to automate the workflow
  - *Reference:* [Create Custom Promptbooks in Security Copilot](https://learn.microsoft.com/en-us/copilot-security/create-custom-promptbooks)

- **Parameter-driven investigations** - Teams need flexible investigation templates that work across different incidents, users, or timeframes
  - *Solution:* Define input parameters using angle bracket notation (e.g., `&lt;IncidentID&gt;`, `&lt;ThreatActor&gt;`, `&lt;number&gt;`) when creating promptbooks, enabling reusable templates that accept dynamic values at runtime

- **Knowledge sharing across teams** - Individual analysts develop effective investigation sequences that others could benefit from
  - *Solution:* Share created promptbooks with the organization during creation or via link from the confirmation pop-up, allowing team members to benefit from customized investigation flows

### Promptbook Management Use Cases

- **Iterative promptbook refinement** - Initial promptbooks need enhancement based on operational experience
  - *Solution:* Access the Promptbook library from the home menu (hamburger icon), select the ellipses next to the owned promptbook, and choose Edit to modify prompts, parameters, tags, or descriptions

- **Promptbook versioning and backup** - Teams need to preserve effective promptbook configurations before modifying them
  - *Solution:* Use the Duplicate option from the ellipses menu to create copies of existing promptbooks, enabling safe experimentation while retaining original versions

- **Promptbook lifecycle cleanup** - Outdated or unused promptbooks clutter the library
  - *Solution:* Delete unwanted promptbooks using the Delete option from the ellipses menu, accessible only to the promptbook owner

- **Quick promptbook execution** - Analysts need rapid access to their custom tools during active investigations
  - *Solution:* Select the prompts icon from the prompt bar, type the promptbook name in the search bar, select it from the list, enter required input parameters, and run

### Collaboration Use Cases

- **Team-wide standardized procedures** - Security operations require consistent investigation methodologies across shifts
  - *Solution:* Create organization-shared promptbooks with defined input parameters, tags, and descriptions, ensuring all analysts follow identical investigation steps with customizable variables

- **Personal workflow optimization** - Individual analysts have unique investigation preferences not suited for team-wide deployment
  - *Solution:* Create promptbooks for personal use only (without sharing), customizing automation flows to individual working styles while keeping them private

---

## References

- [Create Custom Promptbooks in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/create-custom-promptbooks)
- [Using Promptbooks in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/using-promptbooks)
- [Work with Sessions in Security Copilot](https://learn.microsoft.com/en-us/copilot-security/work-with-sessions)
- [Microsoft Security Copilot Prompting Guide](https://learn.microsoft.com/en-us/copilot-security/prompting-in-copilot)
