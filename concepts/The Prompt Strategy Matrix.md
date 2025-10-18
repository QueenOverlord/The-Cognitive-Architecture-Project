---
data: 2025-10-13
"UP:": "[[MOC - Prompt Master]]"
tags:
  - prompt/strategy
  - prompt/diagnostics
  - decision-making
  - mental-model
aliases:
  - The Prompt Strategy Matrix
  - Prompt Triage & Strategy Selection
---
Status: #evergreen

# The Prompt Strategy Matrix: A Field Manual for Tactical Application

> [!summary] Strategic Directive
> This document is the missing link between knowing prompting techniques and mastering their application. It is a strategic framework for **diagnosing the nature of a problem** and mapping it to the most effective prompting architecture. This is not a list of techniques; it is a system for tactical decision-making.

---

## 1. The Core Principle: Diagnose Before You Prescribe

An amateur prompter throws techniques at a problem. An elite prompter first diagnoses the *cognitive domain* of the problem. Every task falls into one of several primary domains. Identifying the domain is the key to selecting the correct strategy.

The core diagnostic question is:

> **"What is the primary cognitive work required to solve this problem: *Generation*, *Transformation*, *Extraction*, or *Reasoning*?"**

---

## 2. The Four Cognitive Domains & Their Corresponding Strategies

### ► Domain 1: Generation (Creating Something from Nothing)
- **Description:** Tasks that require creativity, brainstorming, and the synthesis of new content from a general concept. The output is novel and not strictly derivable from the input.
- **Examples:** Writing a blog post, brainstorming business names, creating a fictional story, drafting a marketing campaign.
- **Primary Risk:** Generic, cliché, or superficial output.
- **Optimal Prompting Architecture:**
    1.  **Persona:** Use an **"Expert Fusion" Persona** to create a unique voice (e.g., "a fusion of a historian and a sci-fi author").
    2.  **Context:** Employ **"World-Building"** to provide a rich, detailed universe for the AI to operate within.
    3.  **Structure:** Use **"Skeleton Prompts"** for long-form content to maintain high-level control over the narrative arc while delegating the detailed writing.

### ► Domain 2: Transformation (Restructuring Existing Information)
- **Description:** Tasks that involve taking existing input and converting it into a different format, style, or structure. The core information exists; the goal is to reshape it.
- **Examples:** Summarizing a long article, translating a text, refactoring code, turning bullet points into a formal email, creating a JSON object from unstructured text.
- **Primary Risk:** Loss of information, introduction of errors, or failure to adhere to the target format.
- **Optimal Prompting Architecture:**
    1.  **Persona:** A highly specific, role-based persona (e.g., "You are a JSON formatter," "You are a technical editor specializing in concise language").
    2.  **Context:** Provide the source material directly and cleanly separated from instructions.
    3.  **Structure:** Use **"In-Context Templating"** with a clear example of the desired output format. This is the most critical step for transformation tasks.

### ► Domain 3: Extraction (Finding a Needle in a Haystack)
- **Description:** Tasks that require finding and isolating specific pieces of information from a large body of text.
- **Examples:** "From the following customer reviews, extract all mentions of 'price' and 'customer service'," "Find the key dates and names in this legal document."
- **Primary Risk:** Missing relevant information (false negatives) or extracting irrelevant information (false positives).
- **Optimal Prompting Architecture:**
    1.  **Persona:** An "Analytical Machine" or "Data Extractor" persona.
    2.  **Context:** Provide the full body of text.
    3.  **Structure:** Be hyper-specific in your instruction. Use **"Few-Shot Prompting"** to show exactly what a correct extraction looks like. Define the output format rigorously (e.g., "Provide the answer as a JSON array of strings"). Include an "out" clause: "If the information is not present, return an empty array."

### ► Domain 4: Reasoning (Deriving a Conclusion Through Logic)
- **Description:** Tasks that require multi-step logic, deduction, planning, or problem-solving. The answer is not immediately present in the input but must be derived.
- **Examples:** Solving a math word problem, debugging code, planning a project timeline, evaluating strategic options.
- **Primary Risk:** Logical fallacies, calculation errors, skipping steps.
- **Optimal Prompting Architecture:**
    1.  **Persona:** A "Logician," "Mathematician," or "Systems Analyst."
    2.  **Context:** Present all variables and constraints clearly.
    3.  **Structure:** This is the prime domain for applying **Cognitive Pressure Frameworks**:
        - **Chain-of-Thought (CoT):** The default for any multi-step problem. *"Think step-by-step."*
        - **Tree of Thoughts (ToT):** Use when multiple solution paths are viable and need to be compared. *"Explore three possible solutions and then select the best one."*
        - **Self-Critique Loops:** Use to double-check the result of a complex reasoning process. *"Review your previous reasoning. Is there a flaw in your logic?"*

---

## 3. The Tactical Advantage in Practice

Before writing any prompt, you will now perform a 10-second "Prompt Triage":

1.  **Diagnose the Domain:** Is this primarily Generation, Transformation, Extraction, or Reasoning?
2.  **Select the Architecture:** Based on the domain, which combination of Persona, Context, and Structure is optimal?
3.  **Execute with Precision:** Write the prompt using the chosen architecture.

This framework elevates you from a prompt user to a prompt strategist. You are no longer guessing; you are making a calculated, tactical decision based on the fundamental nature of the problem itself. This is the secret to consistent, high-level performance.
