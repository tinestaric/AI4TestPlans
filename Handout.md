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

