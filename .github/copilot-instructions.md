# Copilot Instructions for AI Instructions Repository

## Repository Context
Manage AI instruction patterns and templates. Focus: clean, reusable instructions avoiding duplication and drift.

## Core Guidelines
- **File naming**: Use short names with abbreviations (adv, impl, instr, comm, ent, fw, temp, auto)
- **Structure**: Raw content → `collected/` | Curated → `cleaned/`
- **Scope**: Clear outcomes - "Generate REST endpoint" beats "help?"
- **Context**: Seed with specs/schemas vs. reinventing
- **Tasks**: Atomic - one logical task per instruction
- **Instructions**: Be concise and specific, avoid verbose explanations

## Key Tasks
1. **Organize**: Categorize `collected/raw-drops.md` entries
2. **Promote**: Move quality content `collected/` → `cleaned/`
3. **Enhance**: Improve clarity and effectiveness
4. **Template**: Create reusable patterns from successful instructions

## Tool Strategy (Proven Hierarchy)
1. **fetch**: Primary web tool (no limits) - use parallel for efficiency
2. **Standard file ops**: `read_file`, `insert_edit_into_file`, `replace_string_in_file`, `create_file`
3. **brave_search**: Secondary (RATE LIMITED) - use sparingly
4. **MCP**: Read-only operations (AVOID writing/editing)

## Priority Framework
- **High**: Knowledge integration, security patterns, documentation clarity
- **Medium**: Templates, platform compatibility, automation
- **Low**: Experimental approaches, minor optimizations
