# Copilot Setup Instructions for Repository Initialization

## Objective

Initialize the `ai-instructions` repository with a structured set of folders and files to manage, refine, and maintain AI usage instructions.

---

## File Creation Tasks

Create the following files with the specified content:

---

### 1. File: `README.md`

```markdown
# AI Instructions

Centralized, clean, and reusable instruction patterns for AI agents (Copilot, ChatGPT, Claude) with an emphasis on guardrails and instruction quality control.

## Purpose

- Avoid instruction drift and duplication.
- Build reusable, context-free instruction sets.
- Establish and evolve quality guardrails.
- Collect rapidly, organize minimally, and clean only when reuse demands it.

## Structure

- `collected/raw-drops.md`: Raw, unfiltered instruction examples.
- `cleaned/`: Curated and formatted instructions ready for reuse.
- `workflow/copilot-automation.md`: Guidelines for AI agents to assist in maintaining this repository.

## Usage

1. **Daily**: Append new findings to `collected/raw-drops.md`.
2. **Weekly**: Review and promote valuable instructions to the `cleaned/` directory.
3. **Automation**: Utilize `workflow/copilot-automation.md` to guide AI agents in organizing and enhancing instructions.
```

---

### 2. File: `collected/raw-drops.md`

```markdown
# Raw Instruction Drops

Paste all new instruction examples, prompts, and insights here. No formatting or organization required.
```

---

### 3. File: `cleaned/prompt-templates.md`

```markdown
# Prompt Templates

Curated templates for AI prompts, organized by use-case.

## Code Generation

- **Task**: Generate a Python function to calculate factorial.
  **Prompt**: "Write a Python function named `calculate_factorial` that returns the factorial of a given number."

## Documentation

- **Task**: Document a REST API endpoint.
  **Prompt**: "Provide OpenAPI documentation for a GET endpoint at `/users/{id}` that retrieves user information by ID."
```

---

### 4. File: `cleaned/instruction-guides.md`

```markdown
# Instruction Guides

Best practices and guidelines for crafting effective AI instructions.

## General Guidelines

- Be specific and concise.
- Avoid ambiguous language.
- Provide context when necessary.

## Copilot-Specific

- Utilize `copilot-instructions.md` to define repository-wide standards.
- Regularly update instructions to reflect codebase changes.
```

---

### 5. File: `cleaned/examples.md`

```markdown
# Instruction Examples

Real-world examples of effective AI instructions.

## Example 1

- **Context**: Refactoring legacy code.
- **Instruction**: "Refactor the `process_data` function to improve readability and performance without changing its external behavior."

## Example 2

- **Context**: Writing unit tests.
- **Instruction**: "Create unit tests for the `authenticate_user` function covering successful login, failed login, and exception handling."
```

---

### 6. File: `workflow/copilot-automation.md`

```markdown
# Copilot Automation Guidelines

Instructions for AI agents to assist in maintaining and organizing this repository.

## Tasks

1. **Organize `raw-drops.md`**: Categorize entries into relevant sections.
2. **Promote Valuable Instructions**: Identify and move high-quality instructions to the `cleaned/` directory.
3. **Enhance Instructions**: Suggest improvements for clarity and effectiveness.
4. **Identify Duplicates**: Detect and consolidate similar instructions.
```

---

## Final Notes

* Ensure all file names and folder names use lowercase with hyphens.
* Place each file in the correct directory as specified.
* Do not nest folders beyond the structure shown above.

```

---

Once you place this in your repo (e.g., at `.github/copilot-instructions.md`), Copilot can use it as a foundation for structured contributions and maintenance. Let me know when you're ready to push it, and I’ll provide the GitHub file creation links.
