# Prompt Template

## Purpose

Use this template to create a rework plan for an existing feature in your codebase.

## How to Use

1.  Copy the entire content of the "Prompt Template" section below.
2.  Paste it into your AI chat/editor (e.g., Cursor).
3.  Replace the placeholders `[USER: ...]`, `[example-title]` section with the actual code you want to refactor. Provide as much context as possible.
4.  Send the prompt to the AI.

---

I need to rework an existing feature in my project. Existing requirements have changed, and the functionality has similarities and differences to before. I need your help to create a detailed technical plan for this technical rework. Save the plan in .plans/`[example-title]`.md 

Here is the existing feature's code and a brief description of its functionality:

`[USER: PASTE THE RELEVANT CODE FOR THE FEATURE TO BE REWORKED HERE. INCLUDE MULTIPLE FILES IF NECESSARY, AND PROVIDE A BRIEF DESCRIPTION OF WHAT THE FEATURE CURRENTLY DOES AND ANY KNOWN PAIN POINTS.]`

Please analyze the provided code and create a comprehensive Rework Plan. The plan should serve as a technical specification for the engineering team. It must include the following sections:

1. Rationale & Goals:

Explain why this rework is necessary.
State the primary goals and new requirements (e.g., "Pull data from new source", "Reduce cyclomatic complexity", "Enhance testability", "Make the feature easier for new developers to understand").

2. Current State Analysis & Scope:

Briefly summarize the current implementation and its architecture.
Clearly define the scope of the rework, listing the specific files, functions, classes, or modules that will be modified.

3. Identified Issues & Code Smells:

Create a specific, bulleted list of problems in the current code.
For each problem, identify the code smell or anti-pattern (e.g., Duplicated Code, Long Method, Large Class, Tight Coupling, Magic Numbers, Insufficient Error Handling, Lack of Tests).

4. Proposed Rework Strategy:

Describe the high-level approach for the new design.
Detail the specific changes to be made. This could include:
Architectural Changes: (e.g., "Extract business logic into a dedicated service class," "Introduce a data transfer object (DTO) to standardize the API response.")
Design Pattern Application: (e.g., "Apply the Strategy pattern to handle different calculation types," "Use the Factory pattern to create instances of X.")
Key Logic/Algorithm Improvements: (e.g., "Replace the nested loop with a more efficient hash map lookup," "Refactor conditional logic to be polymorphic.")

5. "To-Be" Code Examples:

Provide at least one clear, concise code snippet demonstrating what the reworked code will look like. This should directly address one of the key issues identified in section 3.

6. Testing & Validation Plan:

Outline a strategy to ensure the rework does not introduce regressions.
Specify what types of tests are needed (e.g., "Create characterization tests before reworking," "Add new unit tests for the extracted service class," "Update existing integration tests to reflect the new method signatures.")

7. Potential Risks & Mitigation:

List potential risks (e.g., "Risk of breaking change for API consumers," "Risk of unintended performance degradation in edge cases.")
For each risk, propose a mitigation strategy (e.g., "Mitigation: Introduce the new endpoint alongside the old one and mark the old one as deprecated," "Mitigation: Perform load testing before deployment.")

8. Phased Implementation Steps:

Provide a numbered, step-by-step checklist for a developer to follow to execute the rework safely. This should be a logical sequence of actions. (e.g., 1. Write characterization tests. 2. Extract calculate_price into PricingService. 3. Replace direct calls with the new service method. 4. Run all tests. 5. Remove the old private method.)
For each section, be specific and actionable. Include examples where helpful, and ask clarifying questions if you need more information about any aspect of the project.