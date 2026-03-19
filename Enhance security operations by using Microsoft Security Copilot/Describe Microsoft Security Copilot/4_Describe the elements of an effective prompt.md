# Describe the Elements of an Effective Prompt

In a previous unit, we defined a prompt as the text-based, natural language input you provide in the prompt bar that instructs Microsoft Security Copilot to generate a response. Copilot provides promptbooks and prompt suggestions, which are helpful, particularly if you're just starting an incident investigation. At some point, however, you'll want and need to enter your own prompts. In those cases, the quality of the response that Copilot returns depends in large part on the quality of the prompt used. In general, a well-crafted prompt with clear and specific inputs leads to more useful responses by Copilot.

---

## Elements of an Effective Prompt

Effective prompts give Copilot adequate and useful parameters to generate a valuable response. Security analysts or researchers should include the following elements when writing a prompt.

- **Goal** - specific, security-related information that you need
- **Context** - why you need this information or how you'll use it
- **Expectations** - format or target audience you want the response tailored to
- **Source** - known information, data sources, or plugins Copilot should use

<img width="560" height="470" alt="image" src="https://github.com/user-attachments/assets/16bbef3c-70ce-4966-822a-e2e42e5f9e5d" />

Every good prompt should have a goal. Whether it comes in the form of instructions or questions, it should indicate what you want out of your current session.

For Copilot, context can refer to the time frame, or that you'll use the response for a report. Expectations can include whether you want the response to be in a table format, a list of action steps, a summary, or even a diagram. Source might be useful in specifying which Microsoft plugins you're referring to, if needed. Some plugins require more context to work effectively or supporting plugins to ensure a response when initial responses fail.

Watch this short video for a summary on how to create effective prompts.

---

## Other Prompting Tips

Some things to remember when coming up with your own prompts:

- **Be specific, clear, and concise** as much as you can about what you want to achieve. You can always start simply with your first prompt, but as you get more familiar with Copilot, include more details following the elements of an effective prompt.

  - Basic prompt: `Pearl Sleet actor`
  - Better prompt: `Can you give me information about Pearl Sleet activity, including a list of known indicators of compromise and tools, tactics, and procedures (TTPs)?`

- **Iterate.** Subsequent prompts are typically needed to further clarify what you need or to try other versions of a prompt to get closer to what you're looking for. Like all LLM-based systems, Copilot can respond to the same prompt in slightly different ways.

- **Provide necessary context** to narrow down where Copilot looks for data.

  - Basic prompt: `Summarize incident 15134.`
  - Better prompt: `Summarize incident 15134 in Microsoft Defender XDR into a paragraph that I can submit to my manager and create a list of entities involved.`

- **Give positive instructions** instead of "what not to do." Copilot is geared toward action, so telling it what you want it to do for exceptions is more productive.

  - Basic prompt: `Give me a list of unmanaged devices in my network.`
  - Better prompt: `Give me a list of high-risk unmanaged devices in my network. If they're named "test" remove them from the list.`

- **Directly address Copilot as "You"** as in, "You should ..." or "You must ...", as this is more effective than referring to it as a model or assistant.

While these guidelines can help you get started in creating prompts, it's important to note that you're not limited to forming prompts following the structure of the previous examples. What's great about Copilot is that it's designed to respond to questions or instructions made in your own words (that is, using natural language).

You have the flexibility to adapt these guidelines to your specific needs.

---

## Use Cases and Solutions

### Goal Definition Use Cases

- **Vague threat intelligence requests** - Analysts submit generic actor names without specifying what information they need
  - *Solution:* Include a specific goal in the prompt requesting exactly what security information is needed (e.g., "list of known indicators of compromise and tools, tactics, and procedures (TTPs)")
  - *Reference:* [Microsoft Security Copilot Prompting Best Practices](https://learn.microsoft.com/en-us/copilot-security/prompting-in-copilot)

### Context Provision Use Cases

- **Overly broad incident summaries** - Requests for incident summaries lack specificity about purpose or target audience
  - *Solution:* Add context specifying the intended use (e.g., "into a paragraph that I can submit to my manager") and required output details (e.g., "create a list of entities involved")
  - *Reference:* [Microsoft Security Copilot Effective Prompts](https://learn.microsoft.com/en-us/copilot-security/prompting-in-copilot#elements-of-an-effective-prompt)

- **Time-sensitive investigations** - Analysts need data from specific timeframes or for specific reporting periods
  - *Solution:* Include time frame context in the prompt to narrow the scope of data Copilot searches

### Expectation Setting Use Cases

- **Format-inappropriate outputs** - Copilot returns responses in formats unsuitable for the intended use case
  - *Solution:* Explicitly state expectations for response format (table, list of action steps, summary, diagram) and target audience in the prompt

- **Manager-ready reporting** - Security data needs to be presented to non-technical stakeholders
  - *Solution:* Specify the target audience in expectations (e.g., "that I can submit to my manager") to ensure appropriate technical depth and terminology

### Source Specification Use Cases

- **Multi-plugin ambiguity** - Copilot searches across multiple data sources when the analyst knows the specific source
  - *Solution:* Specify the source by naming the exact plugin or data source (e.g., "in Microsoft Defender XDR") to direct Copilot to the correct information repository
  - *Reference:* [Microsoft Security Copilot Plugins](https://learn.microsoft.com/en-us/copilot-security/manage-plugins)

- **Plugin response failures** - Initial queries to specific plugins return incomplete or failed responses
  - *Solution:* Provide more context about the source and ensure supporting plugins are enabled to ensure comprehensive responses

### Iterative Refinement Use Cases

- **Inconsistent LLM responses** - Copilot generates slightly different responses to identical prompts across sessions
  - *Solution:* Use iterative prompting to further clarify needs and try other versions of prompts to converge on the desired output, accounting for natural LLM variation

### Instruction Optimization Use Cases

- **Negative constraint confusion** - Prompts focusing on what not to do produce ineffective or incomplete results
  - *Solution:* Frame instructions positively toward desired actions, using exception handling for exclusions (e.g., "Give me a list of high-risk unmanaged devices... If they're named 'test' remove them from the list")

- **Indirect addressing inefficiency** - Referring to Copilot as "the model" or "the assistant" reduces response effectiveness
  - *Solution:* Directly address Copilot as "You" using imperative statements ("You should..." or "You must...") for more effective action-oriented responses

### Natural Language Flexibility Use Cases

- **Rigid prompting anxiety** - New users feel constrained by example structures and hesitate to write prompts
  - *Solution:* Leverage Copilot's natural language design to adapt guidelines to specific needs using your own words, without strict adherence to example formats

---

## References

- [Microsoft Security Copilot Documentation](https://learn.microsoft.com/en-us/copilot/security/)
- [Microsoft Security Copilot Prompting Guide](https://learn.microsoft.com/en-us/copilot-security/prompting-in-copilot)
- [Microsoft Security Copilot Effective Prompts](https://learn.microsoft.com/en-us/copilot-security/prompting-in-copilot#elements-of-an-effective-prompt)
- [Microsoft Security Copilot Plugins](https://learn.microsoft.com/en-us/copilot-security/manage-plugins)
- [Microsoft Security Copilot Promptbooks](https://learn.microsoft.com/en-us/copilot-security/using-promptbooks)
