# Instruction Examples

Real-world examples of effective AI instructions and implementation patterns.

## GitHub Copilot Agent Mode Examples

### Example 1: Feature Implementation with Context
- **Context**: Adding OAuth authentication to a Flask application
- **Effective Instruction**: "Add OAuth to our Flask app and write tests. Use Google and GitHub as providers. Follow our existing authentication patterns in `auth/providers.py` and ensure all tests in the `tests/auth/` directory continue to pass."
- **Why It Works**: Specific outcome, provides context files, includes testing requirements, references existing patterns

### Example 2: Multi-File Refactoring
- **Context**: Improving code organization across multiple components
- **Effective Instruction**: "Refactor the user service to extract helper functions into `utils/user_helpers.py`. Maintain the existing API interface and update all imports. Run the test suite after each change."
- **Why It Works**: Clear scope, specifies target structure, maintains compatibility, includes validation step

### Example 3: Debugging with Iterations
- **Context**: Fixing a failing test suite
- **Effective Instruction**: "The tests in `tests/api/test_users.py` are failing after the recent database schema changes. Please analyze the failures, update the test fixtures, and ensure all tests pass."
- **Why It Works**: Specific problem area, context about recent changes, clear success criteria

## GitHub Copilot Coding Agent Examples

### Example 4: Issue-Based Feature Request
**GitHub Issue Content**:
```markdown
### Feature: Add dark mode toggle

**Description**: Implement a dark mode toggle for the user interface

**Acceptance Criteria**:
- [ ] Toggle button in the navigation header
- [ ] Persist user preference in localStorage
- [ ] Apply dark theme to all major components
- [ ] Include accessibility considerations (proper contrast ratios)
- [ ] Add unit tests for the theme switching logic

**Files to Consider**:
- `components/Navigation.tsx`
- `styles/themes.css`
- `hooks/useTheme.ts`

assignees: Copilot
```
- **Why It Works**: Clear feature description, specific acceptance criteria, file guidance, atomic scope

### Example 5: Bug Fix with Reproduction Steps
**GitHub Issue Content**:
```markdown
### Bug: User profile images not loading on mobile

**Expected Behavior**: Profile images should load and display correctly on mobile devices

**Actual Behavior**: Images show broken image icons on mobile Safari and Chrome

**Reproduction Steps**:
1. Navigate to `/profile` page on mobile device
2. Observe profile image area
3. Note broken image icon instead of user photo

**Environment**: 
- Mobile Safari (iOS 15+)
- Mobile Chrome (Android 11+)
- Desktop works correctly

**Acceptance Criteria**:
- [ ] Images load correctly on mobile browsers
- [ ] Proper fallback for failed image loads
- [ ] Responsive image sizing maintained
- [ ] No regression on desktop

assignees: Copilot
```
- **Why It Works**: Clear problem description, specific reproduction steps, environment details, measurable success criteria

## Custom Instructions Examples

### Example 6: Repository-Level Instructions (`.github/copilot-instructions.md`)
```markdown
## Development Standards
- Use TypeScript with strict mode for all new code
- Run `npm run lint` and `npm run test` before committing
- Follow the existing component structure in `src/components/`
- Use Tailwind CSS for styling; avoid custom CSS unless necessary

## Code Patterns
- Prefer functional components with hooks over class components
- Use absolute imports with `@/` prefix for src directory
- Export interfaces from `types/` directory
- Place API calls in `services/` directory with proper error handling

## Quality Requirements
- Minimum 80% test coverage for new features
- Include JSDoc comments for all public functions
- Use semantic commit messages following conventional commits
- Update relevant documentation in `docs/` for new features

## Security Guidelines
- Never commit API keys or secrets
- Validate all user inputs before processing
- Use environment variables for configuration
- Implement proper CORS policies for API endpoints
```
- **Why It Works**: Comprehensive coverage, specific tools and commands, measurable requirements, security focus

### Example 7: Personal Instructions for Code Style
```markdown
- Prefer explicit type annotations in TypeScript
- Use descriptive variable names over abbreviations
- Include error handling for all async operations  
- Generate comprehensive test cases including edge cases
- Add explanatory comments for complex business logic
- Follow functional programming patterns when appropriate
```
- **Why It Works**: Personal preferences, consistent patterns, quality focus

## Workflow Combination Examples

### Example 8: Prototype → Production Workflow
**Phase 1 (Agent Mode)**: "Create a working prototype of a file upload component with drag-and-drop functionality. Focus on core upload mechanics and basic UI."

**Phase 2 (Coding Agent Issue)**:
```markdown
### Polish: File Upload Component Production Readiness

**Context**: Working prototype exists in `components/FileUpload.tsx`

**Requirements**:
- [ ] Add progress indicators for upload status
- [ ] Implement file validation (size, type restrictions)
- [ ] Add error handling and user feedback
- [ ] Create comprehensive test suite
- [ ] Add accessibility features (keyboard navigation, screen reader support)
- [ ] Optimize for mobile devices

assignees: Copilot
```
- **Why It Works**: Builds on previous work, specific enhancement list, production-ready focus

### Example 9: Spec Generation → Implementation
**Phase 1 (Agent Mode)**: "Analyze the existing user management system and draft a technical specification for adding role-based permissions. Include database schema changes, API modifications, and UI updates."

**Phase 2 (Coding Agent Issue)**:
```markdown
### Implement: Role-Based Permissions System

**Specification**: See `docs/rbac-specification.md`

**Implementation Tasks**:
- [ ] Update database schema with roles and permissions tables
- [ ] Modify user model to include role relationships
- [ ] Create middleware for permission checking
- [ ] Update API endpoints with authorization checks
- [ ] Add role management UI components
- [ ] Create migration scripts for existing users

assignees: Copilot
```
- **Why It Works**: Clear specification reference, structured task breakdown, considers migration needs

## Anti-Patterns and Improvements

### Example 10: Vague vs Specific Instructions

**❌ Vague**: "Help me with authentication"
**✅ Specific**: "Implement JWT token refresh logic in the authentication service. When a token expires during an API call, automatically refresh it using the refresh token and retry the original request."

**❌ Vague**: "Fix the bugs"
**✅ Specific**: "The user registration form is not validating email formats correctly. Update the validation in `components/RegistrationForm.tsx` to use proper email regex and show appropriate error messages."

**❌ Vague**: "Make it better"
**✅ Specific**: "Optimize the search function performance by implementing debouncing with 300ms delay and caching results for identical queries. Maintain the existing search API contract."

### Example 11: Context-Rich Instructions

**❌ Without Context**: "Add a new API endpoint"
**✅ With Context**: "Add a new API endpoint `/api/users/{id}/preferences` following our existing patterns in `routes/users.js`. Include GET and PUT methods, validate the preferences schema in `schemas/userPreferences.js`, and add tests similar to `tests/api/users.test.js`."

**❌ Without Context**: "Create a component"
**✅ With Context**: "Create a `NotificationBanner` component following our design system in `components/ui/`. Use the existing `Alert` component as a base and implement the notification patterns shown in `designs/notifications.figma`."
