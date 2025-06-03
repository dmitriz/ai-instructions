# Instruction Guides

Best practices and guidelines for crafting effective AI instructions.

## Core Principles

### Clarity and Specificity
- **Scope the outcome clearly**: "Generate a REST endpoint" beats "help?" - Vagueness breeds hallucination
- **Be specific and concise**: Use short, clear statements for each rule or preference
- **Avoid ambiguity**: Separate unrelated instructions; don't mix multiple concepts in single statements
- **Focus on actionable guidance**: Prioritize instructions that directly affect code generation or workflow

### Context and Iteration
- **Seed with context**: Point to spec files or paste schemas to avoid reinventing solutions
- **Provide necessary context**: Include relevant background information for complex tasks
- **Iterate interactively**: Engage like pair programming with a skilled teammate who needs occasional direction
- **Test and refine**: Verify responses align with standards and adjust instructions accordingly

## Instruction Structure Framework

### Repository-Level Instructions
- **Location**: Place `copilot-instructions.md` in `.github` directory for repository-wide standards
- **Personal Instructions**: Set via Copilot Chat panel for individual preferences
- **Organization Instructions**: (Enterprise) Set organization-wide practices across all repositories

### Essential Instruction Categories
1. **Code Standards**
   - Linting rules and enforcement
   - Testing frameworks and requirements
   - Commit message conventions
   - Code review requirements

2. **Framework Guidelines**
   - Specific patterns for frameworks (React, Next.js, etc.)
   - Library usage conventions
   - Architecture patterns

3. **Naming Conventions**
   - File naming patterns
   - Variable and function naming
   - Directory structure standards

4. **Quality and Security**
   - Testing requirements and coverage expectations
   - Security best practices
   - Accessibility standards
   - Performance guidelines

## AI Agent Interaction Best Practices

### Task Design Principles
- **Keep it atomic**: One logical task per issue; multiple smaller issues scale better than monolithic requests
- **Write crisp acceptance criteria**: Agents read them like specifications
- **Link to relevant files**: Save exploration time by pointing to specific functions or components
- **Leverage incremental feedback**: Use PR comments to request adjustments and refinements

### Workflow Optimization
- **Clear prompts remain essential**: Good tests and small scopes are the secret sauce
- **Use agents in tandem**: Cover full development cycle from prototyping to shipping
- **Maintain human oversight**: Keep humans in loop for architecture, security, and quality decisions

## Quality Assurance Guidelines

### Pre-Implementation Checklist
- **Tests green**: Invest in test coverage; agents rely on tests to validate changes
- **Secrets safe**: Use environment variables, never hardcode sensitive information
- **Review everything**: Agents accelerate work but don't eliminate review responsibility
- **Version control**: Commit early and often, especially with local edits

### Continuous Improvement
- **Update regularly**: As projects evolve, update instructions to reflect current practices
- **Team collaboration**: Encourage team members to contribute to instruction maintenance
- **Monitor outcomes**: Track agent performance and adjust instructions based on results

## Copilot-Specific Guidelines

### Agent Mode vs Coding Agent
- **Agent Mode**: Real-time collaboration within IDE for prototyping, debugging, and exploration
- **Coding Agent**: Asynchronous background processing for feature implementation and routine tasks
- **Combined Usage**: Prototype in agent mode, implement with coding agent for optimal workflow

### Model Selection Strategy
- **OpenAI GPT-4o**: Choose for raw computational power and complex problem-solving
- **Anthropic Claude**: Select for longer context requirements and comprehensive analysis
- **Dynamic switching**: Use model picker to match tool to task requirements

### Advanced Features
- **Model Context Protocol (MCP)**: Extend capabilities with custom tools and external data sources
- **Vision capabilities**: Leverage image processing for visual bug reports and UI mockups
- **Multi-file coordination**: Trust routing logic to handle dependencies and task sequencing
