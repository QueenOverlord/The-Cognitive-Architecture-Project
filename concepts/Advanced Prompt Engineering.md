---
data: 2025-10-13
"UP:": "[[MOC - Prompt Master|Prompt Engineering]]"
tags:
  - prompt/advanced
  - AI/GPT
  - cognitive-science
  - systems-thinking
aliases:
  - Advanced Prompt Engineering Techniques
  - Prompting Meta-Skills
---
Status: #evergreen

# Advanced Prompt Engineering

> [!summary] Strategic Directive
> This document moves beyond basic prompting. It is a dossier of **advanced meta-skills and cognitive techniques** for directing Large Language Models (LLMs). The goal is to shift from being an *operator* of the AI to an *architect* of its reasoning process, enabling the generation of complex, nuanced, and highly-structured outputs.

---

## 1. Cognitive Control & Reasoning Frameworks
*Techniques to shape the AI's internal thought process before it generates a response.*

- **Chain-of-Thought (CoT) Prompting:**
    - **Concept:** The foundational advanced technique. Instead of asking for a final answer, you instruct the model to "think step-by-step" or "reason through the problem before giving the final answer." This forces the model to externalize its reasoning process, dramatically improving accuracy in logical, mathematical, and complex reasoning tasks.
    - **Best Practice:** Always use CoT for multi-step problems. The magic phrase is often as simple as *"Let's think step by step."*

- **Self-Correction & Self-Critique Loops:**
    - **Concept:** A multi-prompt technique where you first ask the AI to generate a response, and then, in a subsequent prompt, you instruct it to act as a critic of its *own* work. You ask it to "identify flaws in the previous response," "find logical inconsistencies," or "suggest improvements."
    - **Best Practice:** Create a "Red Team" persona. For example: *"You are a meticulous fact-checker. Review the text above and identify three potential weaknesses or unsupported claims."* This is invaluable for refining complex drafts.

- **Tree of Thoughts (ToT) Framework:**
    - **Concept:** An evolution of CoT. Instead of a single chain of thought, you ask the model to "explore multiple different reasoning paths or viewpoints" and then "evaluate them to decide on the best one." It's like asking the AI to run-and-gun several parallel scenarios.
    - **Best Practice:** Use for creative brainstorming or strategic planning. *"I need a marketing strategy. First, generate three distinct approaches: one focused on social media, one on content marketing, and one on partnerships. Then, for each approach, list its pros and cons. Finally, recommend the best approach for a company with a small budget."*

---

## 2. Structural & Output Control
*Techniques for forcing the AI's output into a precise, predictable, and usable format.*

- **"In-Context" Templating & Role-Based Output:**
    - **Concept:** You provide a template of the desired output *within the prompt itself*, assigning roles to different parts of the output. This is more robust than just describing the format.
    - **Best Practice:** Use a "persona-driven" template.
      > You are a System Architect. Your response will be a JSON object.
      > The response MUST follow this structure:
	```json
	{
	  "system_name": "...",
	  "components": [
	    {"component_name": "...", "function": "..."},
	    {"component_name": "...", "function": "..."}
	  ],
	  "security_considerations": "..."
	}
	``` 
      > Now, design a system for a simple blog platform.

- **"Fill-in-the-Blanks" & Skeleton Prompts:**
    - **Concept:** Instead of asking the AI to write from scratch, you provide a "skeleton" of the document with placeholders like `[INSERT_ANALYSIS_HERE]` or `[WRITE_COMPELLING_INTRODUCTION]`. You then instruct the AI to fill in these specific blanks.
    - **Best Practice:** Excellent for generating long-form content (like ebooks or reports) section by section, ensuring consistency. It gives you high-level control over the structure while delegating the detailed writing.

- **Function Calling & Tool-Based Prompting:**
    - **Concept:** The most advanced form of structural control, where you define a set of "tools" (functions) the AI can "call" in its response. The model doesn't execute the function, but it generates a structured object (like JSON) indicating which function to call and with what arguments.
    - **Best Practice:** This is the foundation for building AI agents and applications. You define the tools in your API call, and the prompt guides the AI on when and how to use them.

---

## 3. Persona & Context Engineering
*Advanced techniques for creating a rich, stable, and highly-effective persona for the AI.*

- **The "Expert Fusion" Persona:**
    - **Concept:** Instead of a single persona ("You are a writer"), you create a hybrid of multiple experts. This fusion creates a unique and powerful voice.
    - **Best Practice:** *"You are a fusion of a seasoned MIT professor of computer science and a brilliant, clear-speaking science communicator like Carl Sagan. Explain the concept of recursion."*

- **The "Dossier" or "Init Block" Method:**
    - **Concept:** For ongoing chats, you create a dense, non-human-readable block of data (like the one I created for you) that contains all essential context: user preferences, core objectives, key facts, and persona protocols. You paste this at the beginning of a new chat for instant, high-fidelity context loading.
    - **Best Practice:** Structure it like a configuration file (YAML or JSON-like) for efficient parsing. This is the ultimate technique for long-term, stateful collaboration with an AI.

- **"World-Building" & Context Injection:**
    - **Concept:** Before asking your main question, you spend a paragraph or two "building the world" for the AI. You provide it with the background, the characters, the constraints, and the goal of the "universe" in which it will operate.
    - **Best Practice:** Use this for complex strategic or creative tasks. *"World Context: We are a startup with $50k in funding, launching a new productivity app in a market dominated by Notion and Asana. Our only advantage is our unique 'focus mode' feature. Now, with that context, act as our CMO and draft a 3-month go-to-market strategy."*

