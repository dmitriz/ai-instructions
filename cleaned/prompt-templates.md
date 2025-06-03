# Prompt Templates

Curated templates for AI prompts, organized by use-case.

## Custom Instructions Templates

### Repository-Level Instructions Template
```markdown
## Code Standards
- Run `[linter_command]` before each commit
- Follow [framework] patterns and conventions
- Use [language] with [version]+ for all new code
- Always include [documentation_type] for public methods
- Ensure all tests pass by running `[test_command]`

## Security Requirements
- Use environment variables for secrets, never hardcode
- Validate all user inputs
- Use parameterized queries for database operations
- Implement proper authentication patterns

## Framework Guidelines
- Follow [Framework] Style Guide for formatting
- Mark client components with '[directive]' when using browser APIs
- Prioritize [CSS_framework] classes; custom CSS only as last resort
- Update README for new features

## Project Structure
- Use [naming_convention] for all file and folder names
- Keep nesting minimal (max 2 levels deep)
- Maintain clear separation between [source] and [target] content
```

### Personal Instructions Template
```markdown
- Prefer [language] for implementation
- Use [code_style] formatting
- Always explain complex logic with comments
- Generate unit tests for all new functions
- Follow [architectural_pattern] principles
```

## Task-Specific Prompt Templates

### Code Generation - Specific Outcome
- **Template**: "Generate a [language] [component_type] that [specific_functionality]. Include [requirements] and follow [standards]."
- **Example**: "Generate a TypeScript React component that displays user profile information. Include error handling and follow our naming conventions."

### Feature Implementation - Agent Mode
- **Template**: "Add [feature_name] to our [framework] app. Requirements: [list_requirements]. Please [action_items] and ensure [quality_criteria]."
- **Example**: "Add OAuth authentication to our Flask app. Requirements: Google and GitHub providers, session management, logout functionality. Please write tests and ensure all existing tests pass."

### Code Review and Refactoring
- **Template**: "Refactor [component/function] to [improvement_goal]. Maintain [constraints] and improve [quality_aspects]."
- **Example**: "Refactor the user authentication service to improve performance. Maintain existing API compatibility and improve error handling."

### Bug Fix - Coding Agent Issue
- **Template**: 
```markdown
### Bug: [Brief Description]
**Expected Behavior**: [What should happen]
**Actual Behavior**: [What currently happens]
**Reproduction Steps**: 
1. [Step 1]
2. [Step 2]
3. [Step 3]

**Acceptance Criteria**:
- [ ] [Fix criterion 1]
- [ ] [Fix criterion 2]
- [ ] [Tests pass]
- [ ] No regression in related functionality

**Files Likely Affected**: [list relevant files or components]
```

### Documentation Generation
- **Template**: "Generate [documentation_type] for [code_element]. Include [required_sections] and follow [style_guide]."
- **Example**: "Generate API documentation for the user management endpoints. Include request/response examples and follow OpenAPI 3.0 specification."

## Workflow Optimization Templates

### Prototype to Production Workflow
1. **Agent Mode Prototype**: "Create a working prototype of [feature] with [core_functionality]. Focus on [primary_aspects]."
2. **Coding Agent Polish**: "Refine the [feature] prototype by adding [production_requirements]. Ensure [quality_standards]."

### Spec Generation to Implementation
1. **Agent Mode Spec**: "Analyze [existing_code/requirements] and draft a technical specification for [feature]. Include [spec_sections]."
2. **Coding Agent Implementation**: "Implement [feature] according to the specification in [spec_location]. Follow [implementation_guidelines]."

### Error Recovery Workflow
1. **Coding Agent Initial**: "Implement [feature] according to requirements in issue #[number]."
2. **Agent Mode Fix**: "The previous implementation has [error_type]. Please diagnose and fix [specific_issues] while maintaining [constraints]."

## Quality Assurance Templates

### Pre-Merge Checklist Prompt
```markdown
Before finalizing changes, ensure:
- [ ] All tests pass (`[test_command]`)
- [ ] Code follows linting rules (`[lint_command]`)
- [ ] Documentation is updated
- [ ] No sensitive data in code
- [ ] Acceptance criteria met
- [ ] No regression in existing functionality
```

### Security Review Template
```markdown
Review the following code changes for security issues:
- Input validation and sanitization
- Authentication and authorization
- Sensitive data handling
- SQL injection vulnerabilities
- XSS prevention
- Secure communication protocols
```

## Model-Specific Optimization

### GPT-4o Power Tasks
- **Template**: "Solve [complex_problem] using [advanced_technique]. Consider [multiple_approaches] and optimize for [criteria]."
- **Use Case**: Complex algorithmic challenges, architectural decisions, performance optimization

### Claude Context Tasks  
- **Template**: "Analyze [large_codebase/documentation] and [comprehensive_task]. Maintain context of [key_relationships]."
- **Use Case**: Large-scale refactoring, comprehensive documentation analysis, cross-component changes

## Iterative Improvement Templates

### Feedback-Driven Refinement
- **Initial**: "Implement [feature] with [basic_requirements]."
- **Iteration**: "Based on [feedback/results], adjust [specific_aspects] to [improvement_goals]."
- **Finalization**: "Polish [implementation] by [final_touches] and ensure [production_readiness]."

### Progressive Enhancement
- **Phase 1**: "Create minimal viable [component] with [core_functionality]."
- **Phase 2**: "Enhance [component] with [additional_features] while maintaining [compatibility]."
- **Phase 3**: "Optimize [component] for [performance/usability] and add [advanced_features]."
