# Refactor Feature Prompt Template

## Purpose

Use this template to generate a comprehensive refactoring plan for an existing feature in your codebase. This prompt is designed for AI coding assistants like Cursor to analyze existing code and propose a structured, safe, and effective refactoring strategy.

## How to Use

1.  Copy the entire content of the "Prompt Template" section below.
2.  Paste it into your AI chat/editor (e.g., Cursor).
3.  Replace the placeholder `[USER: ...]` section with the actual code you want to refactor. Provide as much context as possible.
4.  Send the prompt to the AI.

---

## Prompt Template

I need to refactor an existing feature in my project. The goal is to improve its maintainability, performance, and readability without altering its external behavior. I need your help to create a detailed technical plan for this refactoring effort.
Save the plan as `[relevant-file-name].md` in the base folder of this project.

Here is the existing feature's code and a brief description of its functionality:

`[USER: PASTE THE RELEVANT CODE FOR THE FEATURE TO BE REFACTORED HERE. INCLUDE MULTIPLE FILES IF NECESSARY, AND PROVIDE A BRIEF DESCRIPTION OF WHAT THE FEATURE CURRENTLY DOES AND ANY KNOWN PAIN POINTS.]`

---

Please analyze the provided code and create a comprehensive **Refactoring Plan**. The plan should serve as a technical specification for the engineering team. It must include the following sections:

*   **1. Rationale & Goals:**
    *   Explain *why* this refactoring is necessary.
    *   State the primary goals (e.g., "Improve performance by 20%", "Reduce cyclomatic complexity", "Enhance testability", "Make the feature easier for new developers to understand").

*   **2. Current State Analysis & Scope:**
    *   Briefly summarize the current implementation and its architecture.
    *   Clearly define the scope of the refactoring, listing the specific files, functions, classes, or modules that will be modified.

*   **3. Identified Issues & Code Smells:**
    *   Create a specific, bulleted list of problems in the current code.
    *   For each problem, identify the code smell or anti-pattern (e.g., Duplicated Code, Long Method, Large Class, Tight Coupling, Magic Numbers, Insufficient Error Handling, Lack of Tests).

*   **4. Proposed Refactoring Strategy:**
    *   Describe the high-level approach for the new design.
    *   Detail the specific changes to be made. This could include:
        *   **Architectural Changes:** (e.g., "Extract business logic into a dedicated service class," "Introduce a data transfer object (DTO) to standardize the API response.")
        *   **Design Pattern Application:** (e.g., "Apply the Strategy pattern to handle different calculation types," "Use the Factory pattern to create instances of X.")
        *   **Key Logic/Algorithm Improvements:** (e.g., "Replace the nested loop with a more efficient hash map lookup," "Refactor conditional logic to be polymorphic.")

*   **5. "To-Be" Code Examples:**
    *   Provide at least one clear, concise code snippet demonstrating what the refactored code will look like. This should directly address one of the key issues identified in section 3.

*   **6. Testing & Validation Plan:**
    *   Outline a strategy to ensure the refactoring does not introduce regressions.
    *   Specify what types of tests are needed (e.g., "Create characterization tests before refactoring," "Add new unit tests for the extracted service class," "Update existing integration tests to reflect the new method signatures.")

*   **7. Potential Risks & Mitigation:**
    *   List potential risks (e.g., "Risk of breaking change for API consumers," "Risk of unintended performance degradation in edge cases.")
    *   For each risk, propose a mitigation strategy (e.g., "Mitigation: Introduce the new endpoint alongside the old one and mark the old one as deprecated," "Mitigation: Perform load testing before deployment.")

*   **8. Phased Implementation Steps:**
    *   Provide a numbered, step-by-step checklist for a developer to follow to execute the refactoring safely. This should be a logical sequence of actions. (e.g., 1. Write characterization tests. 2. Extract `calculate_price` into `PricingService`. 3. Replace direct calls with the new service method. 4. Run all tests. 5. Remove the old private method.)

---

For each section, be specific and actionable. Include examples where helpful, and ask clarifying questions if you need more information about any aspect of the project.