# Raw Instruction Drops

Paste all new instruction examples, prompts, and insights here. No formatting or organization required.

## GitHub Copilot Agent Mode vs Coding Agent - Key Insights (Added: June 3, 2025)

### Core Distinction
- **Agent Mode**: Synchronous, real-time collaboration within IDE (VS Code, JetBrains, Eclipse, Xcode)
- **Coding Agent**: Asynchronous, background processing via GitHub Actions, works through issues and PRs

### Best Practices for AI Instructions

#### Instruction Quality Principles
1. **Scope the outcome clearly**: "Generate a REST endpoint" beats "help?" - Vagueness breeds hallucination
2. **Seed with context**: Point to spec files or paste schemas to avoid reinventing shapes
3. **Iterate interactively**: Like pair programming with a skilled teammate who needs occasional direction
4. **Write crisp acceptance criteria**: The agent reads them like a spec
5. **Keep it atomic**: One logical task per issue. Multiple smaller issues scale better than one behemoth

#### Custom Instructions Framework
- **Repository-Level**: Place `copilot-instructions.md` in `.github` directory
- **Structure Requirements**:
  - Code Standards (linting, testing, commit requirements)
  - Framework Guidelines (React, Next.js, Tailwind CSS patterns)
  - Naming Conventions (files, variables, functions)
  - Project Structure (directory layout, file organization)
  - Testing and Quality (required test commands, coverage expectations)
  - Security and Accessibility (sensitive data handling, accessibility best practices)

#### Instruction Writing Best Practices
- Be specific and concise: Use short, clear statements for each rule
- Avoid ambiguity: Separate unrelated instructions 
- Focus on actionable guidance: Prioritize instructions that directly affect code generation
- Update regularly: As project evolves, update instructions to reflect current practices
- Test responses: Verify that responses align with standards after setting instructions

### Safety and Quality Checklist
- **Tests green**: Both agents rely on tests—invest in coverage or they'll fly blind
- **Secrets safe**: Guard .env files, use secure ephemeral environments
- **Review everything**: Agents accelerate work; they don't eliminate responsibility as reviewer-of-record
- **Version control**: Agent mode edits locally in a branch, so commit early and often

### Workflow Optimization Strategies

#### Routing and Task Management
- **File and Task Selection**: Agent analyzes codebase to determine relevant files and actions
- **Dynamic Workflow Routing**: Adjusts workflow based on feedback (test failures, build errors)
- **Tool and Command Routing**: Uses built-in tools (read_file, edit_file, run_in_terminal) appropriately
- **Context and Session Routing**: Maintains session context across multi-file, multi-step workflows

#### Error Detection and Correction Process
1. **Automatic Test and Build Execution**: Runs relevant tests/builds after code changes
2. **Error Detection and Analysis**: Parses output, identifies failure causes, determines responsible files
3. **Iterative Correction**: Makes additional edits to resolve issues, repeats until complete
4. **User Oversight**: Requires confirmation for terminal commands or non-built-in tools
5. **Streaming and Transparency**: Shows edits in real-time, displays edited files in chat

### Proven Workflow Combinations
1. **Prototype in agent mode, ship with coding agent**: Spike feature branch, then assign polish tasks
2. **Agent mode for spec generation, coding agent for implementation**: Draft design docs, hand off tickets
3. **Coding agent regression fix, agent mode hot patch**: Use agent mode to diagnose and patch failures locally

### Resource Management
- **Agent Mode**: Consumes Copilot premium requests only
- **Coding Agent**: Consumes premium requests + GitHub Actions minutes
- **Strategy**: Queue strategically, treat like coffee—great in moderation, disaster when overflowing

### Custom Instructions Example Template
```
## Code Standards
- Run `npm run lint` before each commit
- Follow Next.js App Router patterns
- Mark client components with 'use client' when using browser APIs or React hooks
- Update README for new features
- Use TypeScript interfaces/types for all props and data structures
- Prioritize Tailwind CSS classes; custom CSS only as a last resort
- Ensure all tests pass by running `npm run test`

## Security Requirements
- Use environment variables for secrets, never hardcode
- Validate all user inputs
- Use parameterized queries for database operations
- Implement proper authentication patterns
```

### Model Selection Guidelines
- **OpenAI GPT-4o**: Raw power for complex tasks
- **Anthropic Claude**: Longer context for comprehensive analysis
- **Switch via model picker**: Choose based on task requirements

### Advanced Features
- **Model Context Protocol (MCP)**: Connect to external data sources and capabilities
- **Vision Models**: Can process screenshots of bugs or mockups in GitHub issues
- **Multi-file Coordination**: Handles dependencies and sequences tasks appropriately

### Quality Assurance Principles
- Clear prompts, good tests, and small scopes remain the secret sauce
- Use both agents in tandem to cover full dev-cycle
- Keep humans in the loop for architecture choices, security reviews
- AI agents replace boring parts of engineering, not engineers themselves

---
