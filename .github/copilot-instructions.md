# Copilot Instructions for AI Instructions Repository

## Repository Context

This repository manages AI instruction patterns and templates. Focus on maintaining clean, reusable instructions while avoiding duplication and instruction drift.

## Coding Guidelines

- Use lowercase with hyphens for all file and folder names
- Maintain clear separation between raw (`collected/`) and curated (`cleaned/`) content
- Keep file structure flat (maximum 2 levels deep)
- Follow markdown best practices with consistent formatting

## AI Instruction Best Practices

### Core Instruction Principles
- **Scope outcomes clearly**: "Generate a REST endpoint" beats "help?" - Vagueness breeds hallucination
- **Seed with context**: Point to spec files or paste schemas to avoid reinventing solutions
- **Be specific and concise**: Use short, clear statements for each rule or preference
- **Focus on actionable guidance**: Prioritize instructions that directly affect code generation or workflow
- **Avoid ambiguity**: Separate unrelated instructions; don't mix multiple concepts in single statements

### Instruction Structure Guidelines
- **Atomic tasks**: One logical task per instruction; multiple smaller instructions scale better
- **Crisp acceptance criteria**: AI agents read them like specifications
- **Context linking**: Reference relevant files or functions to save exploration time
- **Iterative refinement**: Design instructions for feedback-driven improvement

### Quality Assurance Standards
- **Test responses**: Verify that AI responses align with standards after setting instructions
- **Update regularly**: As projects evolve, update instructions to reflect current practices
- **Version control**: Track instruction changes for accountability and rollback capability
- **Review everything**: Instructions accelerate work but don't eliminate review responsibility

## Maintenance Tasks

When working in this repository:

1. **Organizing Raw Content**: Help categorize entries in `collected/raw-drops.md` into appropriate sections
2. **Content Promotion**: Identify high-quality instructions to move from `collected/` to `cleaned/` directories
3. **Quality Enhancement**: Suggest improvements for clarity and effectiveness of existing instructions
4. **Duplicate Detection**: Identify and help consolidate similar or redundant instructions
5. **Template Creation**: Help create reusable templates from successful instruction patterns

## File Organization Priorities

- **collected/raw-drops.md**: Accept any format, no organization required
- **cleaned/**: Ensure consistent formatting and clear categorization
- **workflow/**: Focus on actionable automation guidelines
- **README.md**: Keep overview current with repository structure

## Repository-Specific Instructions

### Content Curation Standards
- Instructions should be specific and actionable
- Avoid ambiguous language and provide context when necessary
- Test instructions before promoting to `cleaned/` directory
- Include real-world examples and anti-patterns where helpful
- Maintain consistency across similar instruction types

### Workflow Automation Principles
- Analyze content for categorization opportunities
- Suggest structural improvements for better organization
- Identify patterns that could become reusable templates
- Help maintain quality standards while preserving rapid collection capability
- Focus on making instructions more reusable and context-free

### Safety and Security Considerations
- Include security best practices in all instruction sets
- Never expose sensitive information in instruction examples
- Validate instruction safety before promotion to cleaned directory
- Maintain human oversight for critical instruction changes

## Advanced AI Agent Integration

### Multi-Agent Workflow Support
- **Agent Mode**: Real-time collaboration for prototyping and refinement
- **Coding Agent**: Asynchronous processing for systematic organization tasks
- **Combined Usage**: Prototype instruction patterns in agent mode, implement with coding agent

### Model-Specific Optimization
- **GPT-4o**: Leverage for complex instruction analysis and pattern recognition
- **Claude**: Utilize for comprehensive content review and long-context tasks
- **Dynamic selection**: Match model capabilities to specific repository tasks
