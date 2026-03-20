# Describe Knowledge Base Connections

Knowledge base connections, a feature of Microsoft Security Copilot currently in preview, allows you to integrate your organization's knowledge base as another source of information. The inclusion of knowledge bases gives Copilot more context, resulting in responses that are more relevant, specific, and customized to your organization.

There are two ways to integrate a knowledge base into Copilot:

- Azure AI Search plugin
- File upload

---

## File Upload

You can upload a file in Microsoft Security Copilot to allow Copilot to refer to the contents of the file for responses when you prompt Copilot for your "uploaded files" or by using the file's name.

To upload a file, the steps are as follows:

1. Navigate to the file upload page by selecting the sources icon in the prompt bar then selecting files from the Manage sources page.

<img width="770" height="630" alt="image" src="https://github.com/user-attachments/assets/cd0728f7-3534-4785-889b-b44d0d66675c" />

2. Select **Upload file** to look for your file. Check that the file you're about to upload is a common text file type like DOCX, MD, PDF, and TXT formats, and that each file doesn't exceed 3 MB. You can upload files, one at a time, as long as the maximum capacity for all the uploaded files doesn't exceed the maximum of 20 MB in total.

3. Wait for the file to appear in Uploads. If an error message appears, correct the problem, and try again.

> Note: Uploaded files are only available to the user account that uploaded them. Uploaded files are stored like the rest of customer data as described in Privacy and data security in Microsoft Security Copilot.

4. To include the file as a source in your current session, select the toggle button so it's lit up (the circle inside the toggle button is in the rightmost position). If you aren't going to use the file yet, or want to exclude it as a source in your current session, select the toggle button so it's greyed out (the circle inside the toggle button is in the leftmost position).

To prompt using the uploaded file, you need to mention "uploaded files" if you want Copilot to reason over your available files. You can also include the file name if you would like to guide Copilot to reason over a specific file. For example, if you want Copilot to check a user account's actions against your organization's data handling policies to find out if any violations were committed, a sample prompt would be:

> Based on the Contoso Data Handling Policy file, list any actions taken by user Preston-123 that might be a violation of the data handling policies. Include a verdict to the action and level of confidence of the verdict. Cite the policy name and section applicable to the verdict.

### Delete a File

To delete a file, select the trash icon next to the file name to delete the file.

### Restricting File Upload (for Owners)

Users assigned the Owner role can choose who are allowed to upload files in owner settings. The options are:

- No one can upload files
- Contributors and Owners can upload files

By default, file upload is available for all users (Contributors and Owners).

<img width="456" height="216" alt="image" src="https://github.com/user-attachments/assets/ac080a86-1432-47f4-b35c-a964d29434e8" />

---

## Azure AI Search Plugin

Azure AI Search is a service that enables you to effectively search, retrieve information, and extract insights from your content, securely and at scale. Common scenarios for using this type of service include document search, data exploration, and chat-style Copilot apps over proprietary data. These use cases are enabled through indexing and querying.

Indexing in Azure AI Search is the process of loading content into your search service and making it searchable. The index is the searchable result of the indexing process.

Querying can happen once an index is populated with searchable content. Your client app sends query requests to a search service and handles responses. All query execution is over a search index that you control.

Through the Azure AI Search plugin, you can bring your own index as a searchable source that you can query using prompts in the Copilot prompt bar.

### Prerequisites

Before you set up the connection to your existing Azure AI index, verify the following requirements:

- The Azure AI Search index is set up for vectorization for use with the text-embedding-ada-002 model.
- The text field in your index must be searchable.
- The title field in your index must be filterable.

One way to get started with setting up an index in the required way is to use integrated vectorization. Refer to Quickstart: Integrated vectorization (preview).

### Configuration Steps

To create the connection to an existing Azure AI Search index, configure the Azure AI Search plugin as follows:

1. Navigate to the setup page for Azure AI Search plugin by selecting the sources icon, selecting plugins, then from the manage plugins windows, selecting the Azure AI Search setup button.

<img width="724" height="628" alt="image" src="https://github.com/user-attachments/assets/09684b59-c937-4212-9ecd-9c75e4f60d59" />

2. The parameters that you configure for the plugin map to information for the Azure AI Search instance, the index within the search instance that will be searched, and the fields associated with the index.

   - **Name of Azure AI Search service** – This is the name of your search service.
   - **Name of index** – This is the name of the index, within your Azure AI search instance, that will be searched.
   - **Name of vector field in index** – This is the name of the field in the index containing the vector of embeddings.
   - **Name of text field in index** – This is the name of the text field in the index. The contents of this field, in your index, represents the text to search. If your index was created using the Import and vectorize data wizard, the name of the field containing the text to search may be referred to as chunk, as a default. The reason is that the wizard will chunk your data so that it doesn't exceed the token limit size of the embedding model. The default index field name, chunk, is referring to a chunk of text.
   - **Name of title field in index** – This is the name of the title field in the index and represents the title of each document to display as a source (optional).
   - **Value** – This is the access identifier for API authentication.

<img width="610" height="692" alt="image" src="https://github.com/user-attachments/assets/ad3a08bc-2e4c-4e13-891d-49f77ae42300" />

3. To obtain the information that you'll use for the plugin settings, you need to go to the Azure portal. Open a new browser tab to go to the Azure portal (https://portal.azure.com).

4. From the Azure portal, search for and navigate to Azure AI Search.

5. The AI Search page lists the search services. From here, you select the search instance you want the plugin to connect to. Before you select it, copy the name and enter it in Azure AI Search service field for the plugin. Copy the name and enter it in the plugin field select the search service.

<img width="904" height="602" alt="image" src="https://github.com/user-attachments/assets/6ba87238-55d3-4035-8740-eb789b8e9c40" />

6. Select the search service whose name you entered in plugin settings page.

7. From the left navigation pane, select **Indexes**.

<img width="771" height="343" alt="image" src="https://github.com/user-attachments/assets/255f30eb-b98e-4873-89de-34f66d42f118" />

8. The indexes page lists the available indexes for a given Azure AI Search service. From the indexes page, copy the name of the index you want to Copilot to search and enter it into the index name field for the plugin.

<img width="974" height="580" alt="image" src="https://github.com/user-attachments/assets/b73eb16b-63c2-40bf-b78d-e110d5b5de44" />

9. Select the index whose name you entered in the plugin settings page. This opens the index page. From here, select the **Fields** tab.

10. The fields tab shows the field names for the index. The field names for the example index named "knowledge-base-bloc-index" and shown in the image that follows may be different than what is shown for your index. Work with the admin who manages your Azure AI Search service for guidance, as needed.

<img width="958" height="576" alt="image" src="https://github.com/user-attachments/assets/b3535301-e5f2-4de4-b39d-3005492aa60c" />

11. Close the index fields page. Then From the left navigation pane, select **Keys**.

12. Copy the "Manage query keys" value for API authentication and enter it in the value field for the plugin, then select save.

<img width="964" height="538" alt="image" src="https://github.com/user-attachments/assets/9adb2b5f-3625-4115-8047-e01dda50ef8a" />

13. Check that all your parameters are correct for the search instance and index you want to connect to then select save.

> Important: Currently, Copilot does not validate your credentials when you save your settings. If they are not correct, you will see an error later when Copilot attempts to run the Azure AI Search plugin. Close the Azure AI Search settings window.

Once connected, prompt Copilot to look for information in the Azure AI Search index. Make sure to mention "Azure AI Search" in the prompt. For example:

- New SOC analysts can ask Copilot about the organization's processes within their Copilot workflows. This can speed up the onboarding process. Sample prompt: `Summarize my organization's multifactor authentication policies in Azure AI Search`.

- SOC analysts can ask Copilot to provide information that helps investigate phishing incidents across large volumes of suspicious emails or files ingested by the index. Sample prompt: `What are the most common email subject headings in my Azure AI Search index that were used in suspected business email compromise (BEC) emails?`

The Azure AI Search plugin performs a semantic and keyword search across the index's contents to find the relevant information so it's advisable to be as specific as you can in prompting. For more on the elements of an effective prompt and other prompting tips, read Describe the elements of an effective prompt.

---

## Use Cases and Solutions

### File Upload Use Cases

- **Quick policy reference** - Analysts need to verify user actions against specific organizational policies during investigations
  - *Solution:* Upload policy documents (DOCX, PDF, TXT, MD, max 3MB per file, 20MB total) via the sources icon, toggle the file active in the session, and prompt Copilot to check actions against the uploaded file by mentioning "uploaded files" or the specific filename
  - *Reference:* [Upload Files in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/upload-files)

- **Personal investigation context** - Analysts have private reference materials not suitable for organization-wide indexes
  - *Solution:* Upload files which are only accessible to the uploading user account, stored according to Privacy and data security guidelines, and can be toggled on/off per session for selective inclusion in prompts

- **Controlled file upload governance** - Organizations need to restrict who can upload files to Copilot
  - *Solution:* Owners configure file upload permissions in owner settings to either "No one can upload files" or "Contributors and Owners can upload files" (default)

- **Temporary file cleanup** - Uploaded files are no longer needed for investigation
  - *Solution:* Select the trash icon next to the file name to delete individual files from the uploads list

### Azure AI Search Integration Use Cases

- **SOC analyst onboarding acceleration** - New analysts need quick access to organizational processes and policies without searching multiple systems
  - *Solution:* Configure the Azure AI Search plugin with a vectorized index (text-embedding-ada-002), then prompt Copilot with "Azure AI Search" mentioned to summarize multifactor authentication policies or other organizational procedures
  - *Reference:* [Azure AI Search Plugin for Security Copilot](https://learn.microsoft.com/en-us/copilot-security/azure-ai-search-plugin)

- **Large-scale phishing investigation** - Analysts need to identify patterns across thousands of suspicious emails ingested into a search index
  - *Solution:* Connect to an Azure AI Search index containing email data using the plugin (service name, index name, vector field, text field, title field, API key), then query for common subject headings in suspected BEC emails

- **Proprietary data integration** - Organizations have internal knowledge bases not available through standard Microsoft plugins
  - *Solution:* Create an Azure AI Search index with required fields (searchable text, filterable title, vectorized embeddings), configure the plugin with parameters from Azure portal (service name, index name, fields, query keys), and enable semantic/keyword search across proprietary content

- **Index field mapping** - Admins need to connect existing Azure AI Search indexes with non-standard field names
  - *Solution:* Map the specific field names from the index (e.g., "chunk" for text fields when using Import and vectorize wizard) to the plugin parameters by consulting with the Azure AI Search administrator and verifying field properties in the Azure portal Fields tab

- **Credential troubleshooting** - Plugin configuration appears correct but queries fail
  - *Solution:* Verify the "Manage query keys" value from Azure portal Keys section is correctly entered in the plugin Value field; note that Copilot does not validate credentials on save, so errors appear only during plugin execution

### Knowledge Base Strategy Use Cases

- **Hybrid knowledge approach** - Organizations need both personal file references and enterprise-wide searchable indexes
  - *Solution:* Use File Upload for individual analyst documents (immediate, private, toggleable) and Azure AI Search Plugin for organizational knowledge bases (scalable, vectorized, shared), selecting the appropriate method based on content sensitivity and scale

---

## References

- [Knowledge Base Connections in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/knowledge-base-connections)
- [Upload Files to Security Copilot](https://learn.microsoft.com/en-us/copilot-security/upload-files)
- [Azure AI Search Plugin for Security Copilot](https://learn.microsoft.com/en-us/copilot-security/azure-ai-search-plugin)
- [Azure AI Search Documentation](https://learn.microsoft.com/en-us/azure/search/)
- [Integrated Vectorization in Azure AI Search](https://learn.microsoft.com/en-us/azure/search/vector-search-integrated-vectorization)
- [Privacy and Data Security in Microsoft Security Copilot](https://learn.microsoft.com/en-us/copilot-security/privacy-data-security)
- [Describe the Elements of an Effective Prompt](https://learn.microsoft.com/en-us/copilot-security/prompting-in-copilot)
