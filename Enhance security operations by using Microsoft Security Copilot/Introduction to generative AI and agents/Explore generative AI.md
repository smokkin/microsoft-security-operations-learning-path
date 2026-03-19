# Explore Generative AI

In this exercise, you'll use a chat playground to interact with a generative AI model. The goal of this exercise is to explore the effect of system prompts, model parameters, and grounding models with data.

This exercise should take approximately 15 minutes to complete.

---

## Chat with a Model

Let's start by using a chat interface to submit prompts to a generative AI model. In this exercise, we'll use a small language model that is useful for general chat solutions in low bandwidth scenarios.

> Note: If your browser supports WebGPU, the chat playground uses the Microsoft Phi 3 Mini model running on your computer's GPU. If not, the SmolLM2 model is used, running on CPU - with reduced response-generation quality. Performance for either model may vary depending on the available memory in your computer and your network bandwidth to download the model. After opening the app, use the ? (About this app) icon in the chat area to find out more.

1. In a web browser, open the Chat Playground at https://aka.ms/chat-playground.
2. Wait for the model to download and initialize.

> Tip: The first time you download a model, it may take a few minutes. Subsequent downloads will be faster. If your browser or operating system does not support WebGPU models, the fallback CPU-based model will be selected (which provides slower performance and reduced quality of response generations).

3. When the model is ready, enter a prompt such as `Who was Ada Lovelace?`, and review the response (which may take some time to be generated).
   
   <img width="525" height="452" alt="image" src="https://github.com/user-attachments/assets/7cf8fdf2-79a3-496a-8913-750294c29475" />

5. Enter a follow-up prompt, such as `Tell me more about her work with Charles Babbage.` and review the response.
   
   <img width="525" height="452" alt="image" src="https://github.com/user-attachments/assets/625a6aff-31dc-4cda-848a-99dca791310b" />

> Note: Generative AI chat applications often include chat history in the prompt; so the context of the conversation is retained between messages (for example, in the follow-up prompt *Tell me more about her work with Charles Babbage.*, "her" is interpreted as relating to Ada Lovelace).

5. At the top of the chat pane, use the **New chat (💬)** button to restart the conversation. This removes all conversation history.
6. Enter a new prompt, such as `Who was Alan Turing?` and view the response.
7. Continue the conversation with prompts such as `What is the Turing test?` or `What is a Turing machine?`.
   
   <img width="525" height="452" alt="image" src="https://github.com/user-attachments/assets/7eca3f5b-1a13-4508-b298-0f286ddb3e17" />

---

## Experiment with System Prompts

A system prompt is used to provide the model with an overall context for its responses. You can use the system prompt to provide guidelines about format, style, and constraints about what the model should and should not include in its responses.

1. At the top of the chat pane, use the **New chat (💬)** button to restart the conversation. Then enter a new prompt, such as `What was ENIAC?` and view the response.
   
   <img width="525" height="452" alt="image" src="https://github.com/user-attachments/assets/1a8dcd03-6ead-456c-896e-8739f1ad50a0" />

3. Start a new chat, and then in the pane on the left, in the **Instructions** text area, change the system prompt to: `You are an AI assistant that helps people find information about computing history. IMPORTANT: You must answer concisely with a single paragraph.`

4. Now try the same prompt as before (`What was ENIAC?`) and review the output.
   
   <img width="525" height="452" alt="image" src="https://github.com/user-attachments/assets/877bcfed-ba9c-4afb-8a1a-ea059c595ff9" />

6. Continue to experiment with different system prompts to try to influence the kinds of response returned by the model.

> **Note:** Smaller models like SmolLM2 can be less responsive to explicit system prompts than larger ones. You may observe some cases where the system instructions are not followed precisely.

5. When you have finished experimenting, change the system prompt back to `You are an AI assistant that helps people find information.`

---

## Experiment with Model Parameters

Model parameters control how the model works, and can be useful for restricting the size of its responses (measured in tokens) and controlling how "creative" its responses can be.

1. Use the **New chat (💬)** button to restart the conversation.
2. In the pane on the left, next to the selected model, select **Parameters (🝰)**.
   <img width="525" height="425" alt="image" src="https://github.com/user-attachments/assets/0f93f858-555c-4f2e-884d-c5226967d9d0" />
4. Review the parameter settings; then, without changing them, enter a prompt like `Explain Moore's law.` and review the response.
   
6. Experiment by changing the parameter values and repeating the same prompt. You should see some differences in behavior from the model. For example, changing the Temperature modifies the randomness of the model's word selection, changing the "creativity" of the responses (to the point that too high a temperature can cause nonsensical responses).

> Note: Parameters changes can have less effect on smaller models.

5. When you've finished experimenting, reset the parameters to their default values.

---

## Ground Responses with Data

Generative AI is the foundation for agentic solutions; in which AI agents can assist you and act on your behalf. Agents are more than general purpose chat apps. They usually have a particular focus, and use knowledge and tools to perform their duties.

For example, let's suppose an organization wants to use a generative AI agent to help employees with expense claims.

1. Change the system prompt to `You are a helpful AI assistant who supports employees with expense claims.` and start a new chat conversation.
2. Enter the prompt `How do I submit a claim?` and view the response.

The response is likely to be generic. Accurate; but not particularly helpful to the employee. We need to give the agent some knowledge about the company's expense policies and procedures.

3. Open a new browser tab, and view the expenses guide at https://aka.ms/expenses-txt. We'll use this to ground the model, so it has some context for questions about expenses.

> **Note:** This is a very small document for the purposes of this exercise. In a real scenario, an AI agent might have access to large volumes of data; usually in the form of a vector index.

4. Save the expenses.txt file on your local computer.
5. Return to the tab containing the chat playground, and in the pane on the left, expand the **Tools** section if it's not already expanded.
6. Upload the expenses.txt file. The chat is automatically restarted.
7. Enter the same expenses-related prompt (`How do I submit a claim?`) and view the response.

This time the response should be informed by the information in the expenses data source.

8. Try a few more expenses-related prompts, like `How much can I spend on a taxi?`, `What about a hotel?` or `Can I claim the cost of my dinner?`

> Note: The small amount of data and the limited capabilities of the small models used in this exercise may result in some inaccurate responses; but the principle of retrieving contextual information, using it to augment the prompt, and generating responses based on the data is a common pattern in generative AI solutions known as Retrieval Augmented Generation (or RAG).

---

## Explore Client Code to Use a Model

You've seen how a model can be used in a pre-provided chat playground, but how do developers build apps and agents that submit prompts to models and process responses?

One of the most commonly used application programming interfaces (APIs) used to develop apps that work with LLMs is the OpenAI API - and in particular the Python SDK for the OpenAI API.

1. Navigate away from the Chat Playground app to the Model Coder app at https://aka.ms/model-coder and wait for the Python environment and model to load.

This app provides an in-browser sandbox with a Python library that encapsulates the most common classes in the OpenAI SDK. You'll use it to write and run real Python code that submits prompts to a local LLM running in the browser.

2. When the model has loaded, ensure the **Blank Page** sample is selected and that there is no existing code in the Editor pane. Then add the following code:

```python
# import namespace
from openai import OpenAI

# Initialize the OpenAI client
openai_client = OpenAI(
  base_url="http://localwllama",
  api_key="key123"
)
         
# Get a response
completion = openai_client.chat.completions.create(
  model="smollm2",
  messages=[
      {
          "role": "system",
          "content": "You are a helpful AI assistant that answers questions and provides information."
      },
      {
          "role": "user",
          "content": "Tell me about the ELIZA chatbot."
      }
  ]
)
print(completion.choices[0].message.content)
```

This code uses the OpenAI ChatCompletions API to:

- Connect to the local WLLMA environment in the browser using an authentication key
- Submit the following prompts to the local smollm2 model:
 - System prompt: "You are a helpful AI assistant that answers questions and provides information."
 - User prompt: "Tell me about the ELIZA chatbot."

Use the **▶ (Run code)** button on the toolbar to run the Python code.

The code runs in the Terminal pane at the bottom of the screen (it may take a minute or so to run).

Review the response from the model.

> Note: The model used in this app is a small language model with very limited training data. Its responses may not be accurate. However, the point of the exercise is to learn to use the OpenAI SDK syntax to submit prompts and receive responses - regardless of how innacurate they may be!

The ChatCompletions API is commonly used in generative AI applications. However, a newer Responses API is becoming increasingly popular because of its versatility and simpler structure.

Let's modify the code to use the newer Responses API.

Replace the code in the Editor pane with this code:

```python
# import namespace
from openai import OpenAI

# Initialize the OpenAI client
openai_client = OpenAI(
    base_url="http://localwllama",
    api_key="key123"
)

# Get a response
response = openai_client.responses.create(
    model="smollm2",
    instructions="You are a helpful AI assistant that answers questions and provides information.",
    input="Explain the Turing test."
)
print(response.output_text)
```

This code uses the OpenAI Responses API to connect to the same model as before, this time submitting the following prompts:

- System prompt (instructions): "You are a helpful AI assistant that answers questions and provides information."
- User prompt (input): "Explain the Turing test."

Run the modified code and review the output in the Terminal pane.

---

## Summary

In this exercise, you explored a generative AI model in a chat playground. You've seen how a model's responses can be affected by changing the system prompt, configuring model parameters, and by adding data. Finally, you've explored how developers can use models from client applications through the OpenAI-compatible APIs in Python.

The interface and techniques used in this exercise are similar to those in Microsoft Foundry portal; a platform for building AI apps and agents in the Microsoft Azure cloud. You can use the OpenAI SDK to connect to Microsoft Foundry endpoints and work with your models there.

---

## Use Cases and Solutions

### ChatCompletions API Use Cases

- **Integrating LLMs into Python applications** - Developers need to programmatically submit prompts and receive responses from local or remote language models
  - *Solution:* Use the OpenAI ChatCompletions API with the Python SDK to initialize a client with base URL and API key, create completions with system and user messages, and extract response content

- **Maintaining conversation context** - Applications require structured message history with distinct roles for system instructions and user queries
  - *Solution:* Format prompts as a messages array with role-based objects (`system` for behavior definition, `user` for queries) and pass to `chat.completions.create()`

### Responses API Use Cases

- **Simplifying API code structure** - Existing ChatCompletions implementations require verbose message array formatting
  - *Solution:* Migrate to the Responses API which uses direct `instructions` parameter for system prompts and `input` parameter for user prompts, reducing code complexity

- **Rapid prototyping of AI features** - Developers need quick integration without managing complex message structures
  - *Solution:* Use `openai_client.responses.create()` with simplified parameters to submit prompts and retrieve `output_text` directly

### Local Model Deployment Use Cases

- **Browser-based AI development** - Developers need to test AI integrations without cloud dependencies or API costs
  - *Solution:* Connect to local WLLMA environment using `base_url="http://localwllama"` with authentication key, enabling in-browser model execution via OpenAI-compatible endpoints

- **Testing with lightweight models** - Applications require validation of SDK syntax and integration patterns before production deployment
  - *Solution:* Use small language models like smollm2 in local environments to verify code functionality, accepting response inaccuracies as trade-off for development efficiency

---

## References

- [Azure AI Foundry Documentation](https://learn.microsoft.com/en-us/azure/ai-foundry/)
- [Azure OpenAI Service Documentation](https://learn.microsoft.com/en-us/azure/ai-services/openai/)
- [OpenAI API Reference](https://platform.openai.com/docs/api-reference)
- [OpenAI Python SDK](https://github.com/openai/openai-python)
- [Chat Completions API Guide](https://platform.openai.com/docs/guides/chat-completions)
- [Responses API Documentation](https://platform.openai.com/docs/api-reference/responses)
- [Microsoft Foundry Portal](https://learn.microsoft.com/en-us/azure/ai-foundry/)
