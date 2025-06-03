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

## Repository Setup

This repository follows a structured approach to organizing AI instructions:

### File Structure

```
README.md                           # Overview and setup instructions
.gitignore                         # Ignore patterns for JS/Python
collected/
  raw-drops.md                     # Unfiltered instruction examples
cleaned/
  prompt-templates.md              # Curated prompt templates
  instruction-guides.md            # Best practices and guidelines
  examples.md                      # Real-world instruction examples
workflow/
  copilot-automation.md           # AI agent maintenance guidelines
.github/
  copilot-instructions.md         # Copilot behavior instructions
```

### Quick Start

1. **Add new findings**: Append to `collected/raw-drops.md`
2. **Organize content**: Use templates in `cleaned/` directory
3. **AI assistance**: Reference `workflow/copilot-automation.md` for maintenance tasks

### File Guidelines

- Use lowercase with hyphens for all file and folder names
- Keep nesting minimal (max 2 levels deep)
- Maintain clear separation between raw and curated content
