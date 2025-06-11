# 🧠 Workshop Handout: Build Your Own AI Pipeline and Let It Draft Your Test Plans

---

## ✅ Prerequisite
**✔ Bring 1–2 user stories from your own work or use our examples below.**

### 📌 Sample User Stories (if you need them):
## User Story 1
  **As a** production planner **I want to** be able to setup extended texts for items, resources and standard text for assembly documents, **so that** I can add these extended texts as additional information to items, resources and standard text on any assembly document, as line(s) underneath the related item, resource or standard text line.

## User Story 2
  **As a** production planner **I want to** be able add extended texts as additional information to items, resources and standard text on any assembly document as line(s) underneath the related item, resource or standard text line **so that** I do not need to type that in myself.

## User Story 3
  **As a** production planner **I want to** be able add items, resources and standard text to any assembly document **so that** I the extended automatically is added to the document as line(s) underneath the related item, resource or standard text line.

### Additional information
- [Assembly Management - Business Central | Microsoft Learn](https://learn.microsoft.com/en-us/dynamics365/business-central/assembly-assemble-items)
- [Add extended text - Business Central | Microsoft Learn](https://learn.microsoft.com/en-us/dynamics365/business-central/ui-how-define-ext-text)
- [Dynamics 365 Business Central: How to add Extended Text | Yun Zhu](https://yzhums.com/13060/)
- [Using Item Extended Text in Dynamics 365 Business Central - Crestwood Associates](https://www.crestwood.com/blog/using-item-extended-text-in-dynamics-365-business-central/)
  - Only one that discusses the option Automatic Ext. Text on the item card 

---

## 🏁 Step 1 – Try on Your Own (Cold Prompt)
**🎯 Goal:** Prompt your first test plan using just the user story, no guidance. This helps establish a baseline and understand the model's default output with minimal direction.

**📝 Prompt Used:**
```
<write your original prompt here>
```
**(Remember to save the output from this prompt for comparison later!)**

**🧪 Outcome Notes:**
- Was the output relevant to the user story?
- What key information or test types were missing (e.g., positive tests, negative tests, boundary conditions)?
- How was the output structured? Was it easy to read and understand?
- Did the model include any specific edge cases or less obvious scenarios?
- Was the generated plan immediately actionable for a tester, or would it require significant refinement?

---

## 🧱 Step 2 – Add Structure to Your Prompt
**Use the 5 prompt components to refine your input.**

> 💡 For more on structuring prompts, see ["How to be a Prompt Engineer" (YouTube)](https://www.youtube.com/watch?v=q8xpDwjyNLY)

| Component            | Purpose | Your Version | Example |
|---------------------|---------|--------------|---------|
| **Instructions**     | What you want it to do | | "Create a comprehensive test plan for the following user story" |
| **Steps**            | Break it down if needed | | "1. Analyze the user story 2. Identify test scenarios 3. Define test cases" |
| **Format Requirements** | How to structure output | | "Use Gherkin syntax with Given-When-Then format" |
| **Examples**         | Show desired output style | | "Example: Given a user is logged in, When they click logout, Then they should be redirected to login page" |
| **Notes**            | Constraints and context | | "Focus on edge cases, include both positive and negative scenarios" |

### 💡 Pro Tips:
- Be specific about what you want
- Use action verbs (analyze, create, evaluate)
- Specify the format explicitly
- Include quality criteria

**📝 Final Prompt (with structure):**
```
<space for writing or pasting prompt>
```

**🔄 Compare Outputs:**
Run your structured prompt. How does the output compare to the one from your "cold prompt" in Step 1?
- Is it more comprehensive?
- Is the formatting better?
- Did it follow your instructions more closely?

---

## 🔧 Step 3 – Generate a System Prompt Automatically
Use the provided tool to generate a system prompt using your components.

- Try [OpenAI Playground](https://platform.openai.com/playground/prompts) or [Azure AI Foundry](https://ai.azure.com/) to experiment with system prompts.

Compare outcomes:
- User prompt only
- System + User prompt

**📊 Notes:**
- How did it change the tone or structure?
- Was it easier to guide?

---

## 🤝 Step 4 – Peer Feedback (ATDD Lens)

Share your results with a peer or group. Use this checklist to evaluate the output:

| ✅ Criteria                                  | Yes / No | Comments |
|--------------------------------------------|----------|----------|
| Clear and actionable test plan?             | ✅ / ❌  |          |
| Matches acceptance criteria?                | ✅ / ❌  |          |
| Covers edge cases or boundaries?            | ✅ / ❌  |          |
| Testable/measurable language?               | ✅ / ❌  |          |
| No vague or redundant parts?                | ✅ / ❌  |          |

---

## 🔁 Step 5 – Improve Prompt Using Feedback

```
<space for improved prompt>
```

---

## 🧪 Step 6 – Try Different Models

Try the same prompt across multiple models.

> 💡 Explore more models at [GitHub Marketplace Models](https://github.com/marketplace/models)

### 🎯 What to Look For:
- **Speed vs Quality trade-off**
- **Token efficiency** (how concise is the output?)
- **Instruction following** (does it stick to your format?)
- **Creativity vs Consistency**

| Model      | Output Summary      | Strengths             | Weaknesses            | Best Use Case |
|------------|---------------------|------------------------|------------------------|---------------|
| GPT-4      |                     |                        |                        |               |
| GPT-3.5    |                     |                        |                        |               |
| Claude     |                     |                        |                        |               |
| Mini/Nano  |                     |                        |                        |               |

---

## 🧠 Step 7 – Prompt for Reasoning

Try a different task that benefits from reasoning.  
_Example: "Evaluate whether the test plan sufficiently covers negative cases. Provide feedback with reasoning."_

### 🎯 Sample Reasoning Tasks:
1. **Gap Analysis:** "Analyze this test plan and identify missing test scenarios. Explain why each scenario is important."
2. **Risk Assessment:** "Review these test cases and rank them by risk level. Justify your rankings."
3. **Test Optimization:** "Suggest which tests could be automated vs manual. Provide reasoning for each recommendation."

**📝 Prompt:**
```
<your prompt>
```

**📊 Observations:**
- What changed?
- What did the model "understand" better?
- How detailed was the reasoning?
- Did it catch nuances you missed?

### 🤔 How Reasoning Models Differ

| Traditional Models | Reasoning Models |
|-------------------|------------------|
| Need explicit step-by-step guidance | Less need to "hold its hand" |
| Rely heavily on examples | More value in constraints, less in examples |
| Best for structured tasks | Excel at analysis and evaluation |
| Follow patterns strictly | Can adapt and think through problems |
| Output focused | Process + Output focused |

### 📐 Guidelines for Reasoning Model Prompts

| Component | Purpose | Example |
|-----------|---------|---------|
| **Instruction** | What's the goal? | "Analyze this test plan for completeness" |
| **Constraints** | Format? Tone? Limits? | "Focus on edge cases, be concise" |
| **Preferences** | What to prioritize? | "Prioritize security over performance tests" |
| **Autonomy Range** | Should the model "think" or follow? | "Feel free to suggest alternative approaches" |
| **Optional Revision Loop** | Can it check or improve itself? | "Review your suggestions and refine if needed" |

---

## 🔄 Step 8 – Pre/Postprocess Manually

Break the problem down:
- **Preprocess:** 
  - Rewrite the user story for clarity
  - Extract key components (actor, action, outcome)
  - Convert into acceptance criteria
  - Identify implicit requirements
- **Postprocess:** 
  - Reorganize raw output into standard format
  - Remove hallucinations or irrelevant content
  - Add missing edge cases
  - Validate against original requirements

**🛠️ Example Preprocessing:**
```
Original: "User wants to search products"
↓
Preprocessed: 
- Actor: Registered/Guest User
- Action: Search for products using keywords
- Acceptance Criteria:
  • Search returns relevant results
  • Results are paginated
  • Search history is saved (if logged in)
```

**🛠️ Notes:**
```
<space>
```

---

## 🪄 Step 9 – Pre/Postprocess with Prompts and Models

Use different prompts and models for each stage of the pipeline.

| Stage         | Model Used | Prompt Summary           | Output Quality Notes |
|---------------|------------|---------------------------|----------------------|
| Preprocess    | Mini       | Extract key elements      |                      |
| Generate Plan | GPT-4      | Test plan generation      |                      |
| Evaluate Plan | Reasoning  | Spot gaps, improve plan   |                      |

---

## 💡 Final Thoughts / Next Steps

### 🎯 Key Takeaways:
- [ ] Structured prompts produce better results
- [ ] Different models excel at different tasks
- [ ] Preprocessing improves output quality
- [ ] Reasoning models need different prompting strategies
- [ ] Iteration is key to prompt engineering

### 🚀 Action Items:
1. What's one technique you'll implement immediately?
2. Which model fits your use case best?
3. How will you measure prompt effectiveness?

### 🔗 Resources:
- [How to be a Prompt Engineer](https://www.youtube.com/watch?v=q8xpDwjyNLY)
- [Prompt Engineering Guide](https://www.promptingguide.ai/)
- [OpenAI Best Practices](https://platform.openai.com/docs/guides/prompt-engineering)
- [Anthropic's Prompt Engineering](https://docs.anthropic.com/claude/docs/prompt-engineering)

### 💭 Reflection Questions:
- What surprised you most about prompt engineering?
- How might this change your testing workflow?
- What other tasks could benefit from this approach?
