# Describe How Microsoft Security Copilot Processes Prompt Requests

So now that there's a basic understanding of plugins, capabilities, and how the user interacts with Microsoft Security Copilot through prompts, it's worth taking a look under the hood to see how these components come together to process a prompt request and help security analysts.

---

## Process Flow

When a user submits a prompt, Copilot processes that prompt to generate the best possible response. The diagram that follows illustrates, at a high level, steps that Copilot takes to process the prompt and generate a response.

<img width="560" height="470" alt="image" src="https://github.com/user-attachments/assets/255ea7d0-acb3-4fc8-a823-4559e62d5c55" />

1. **Submit a prompt** - The process starts when a user submits a prompt in the prompt bar.

2. **Orchestrator** - Security Copilot sends the information to the Copilot backend referred to as the orchestrator. The orchestrator is Copilot's system for composing capabilities together to answer a user's prompt. It determines the initial context and builds a plan using all the available capabilities (skills).

3. **Build context** - Once a plan is defined and built, Copilot executes that plan to get the required data context to answer the prompt.

4. **Plugins** - In the course of executing the plan, Copilot analyzes all data and patterns to provide intelligent insights. This includes reasoning over all the plugins and sources of data, enabled and available to Copilot.

5. **Responding** - Copilot combines all the data and context and uses the power of its advanced LLM to compose a response using language that makes sense to a human being.

6. **Response** - Before the response can be sent back to the user, Copilot formats and reviews the response as part of Microsoft's commitment to responsible AI.

7. **Receives response** - The process culminates with the user receiving the response from the Copilot.

---

## Process Log

During this process, Copilot generates a process log that is visible to the user. The user can see what capability is used to generate the response. This is important because it enables the user to determine whether the response was generated from a trusted source. In the screenshot that follows, the process log shows that Copilot chose the Incident Analysis capability. The process log also shows that the final output went through safety checks, which is part of Microsoft's commitment to responsible AI.

<img width="550" height="470" alt="image" src="https://github.com/user-attachments/assets/70750401-3915-4c21-bd22-0868e34e8e37" />

---

## Use Cases and Solutions

### Prompt Processing Use Cases

- **Complex multi-source security investigations** - Security analysts need to gather and synthesize data from multiple security tools and plugins to answer a single query
  - *Solution:* The orchestrator automatically builds a plan using all available capabilities (skills), executes the plan to gather required data context from enabled plugins, and composes a unified response without manual tool switching
  - *Reference:* [Microsoft Security Copilot Orchestrator](https://learn.microsoft.com/en-us/copilot/security/copilot-security-terminology#orchestrator)

- **Verifying response authenticity and sources** - Analysts need to validate that Copilot responses are based on trusted security data sources
  - *Solution:* Review the visible process log to see exactly which capability was used to generate the response, enabling determination of whether the response came from a trusted source
  - *Reference:* [Microsoft Security Copilot Process Log](https://learn.microsoft.com/en-us/copilot-security/copilot-security-terminology)

- **Ensuring responsible AI outputs** - Organizations need assurance that AI-generated security guidance meets safety and compliance standards
  - *Solution:* Copilot automatically formats and reviews all responses through safety checks before delivery, as part of Microsoft's commitment to responsible AI and visible in the process log
  - *Reference:* [Microsoft Responsible AI Principles](https://www.microsoft.com/en-us/ai/responsible-ai)

- **Context-aware security analysis** - Analysts submit prompts requiring deep understanding of their security environment
  - *Solution:* The orchestrator determines initial context, builds an execution plan, and Copilot reasons over all enabled plugins and data sources to provide intelligent insights tailored to the specific environment
  - *Reference:* [Microsoft Security Copilot Plugins](https://learn.microsoft.com/en-us/copilot-security/manage-plugins)

- **Natural language security queries** - Security teams need to query complex security data without learning specialized query languages
  - *Solution:* Submit prompts in natural language through the prompt bar; Copilot uses its advanced LLM to compose responses using human-readable language while processing the technical complexity in the backend
  - *Reference:* [Microsoft Security Copilot Prompting](https://learn.microsoft.com/en-us/copilot-security/prompting-in-copilot)

---

## References

- [Microsoft Security Copilot Documentation](https://learn.microsoft.com/en-us/copilot/security/)
- [Microsoft Security Copilot Terminology](https://learn.microsoft.com/en-us/copilot/security/copilot-security-terminology)
- [Microsoft Security Copilot Process Flow](https://learn.microsoft.com/en-us/copilot-security/how-copilot-works)
- [Microsoft Security Copilot Plugins](https://learn.microsoft.com/en-us/copilot-security/manage-plugins)
- [Microsoft Responsible AI](https://www.microsoft.com/en-us/ai/responsible-ai)
- [Microsoft Security Copilot Prompting Best Practices](https://learn.microsoft.com/en-us/copilot-security/prompting-in-copilot)
