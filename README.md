# Pull Request Submission Checklist

## General

- [ ]  Ensure there is a ticket created for the change in your tracking system (e.g., Jira). All changes—whether bugfixes, hotfixes, or new features—must be linked to a ticket.
- [ ]  Create the branch using a standard naming convention (e.g., `feature/<JIRA_TICKET_ID>-short-description` or `bugfix/<JIRA_TICKET_ID>`).
- [ ]  Ensure the pull request addresses changes for the referenced ticket.

## Code Quality

- [ ]  Perform a self-code review and check for:
    - [ ]  Commented-out code (See why this matters: https://kentcdodds.com/blog/please-dont-commit-commented-out-code)
    - [ ]  Typos and grammatical errors
    - [ ]  Overly complex logic or unnecessary abstractions
    - [ ]  Unclear variable or function names
    - [ ]  Potential bugs or missing edge case handling
    - [ ]  Security vulnerabilities (SQL injection, XSS, secrets exposure)
    - [ ]  Performance bottlenecks
    - [ ]  Proper logging (use appropriate log levels, avoid logging sensitive info)
    - [ ]  Code formatting (ensure linting, Prettier/ESLint rules are followed)
    - [ ]  Unused dependencies or imports
    - [ ]  Duplicated code and anti-patterns

## Testing

- [ ]  Verify all unit and integration tests pass.
- [ ]  Test your changes thoroughly in your local environment before submission. When possible, deploy and test in a staging environment.
- [ ]  If introducing a new feature, ensure new unit/integration tests are included.
- [ ]  If modifying existing behavior, confirm related tests are updated accordingly.
- [ ]  If applicable, ensure contract/API tests are updated.

## Documentation

- [ ]  Write a comprehensive description of your changes, including:
    - [ ]  The business rationale for the code changes
    - [ ]  Screenshots of UI changes (if applicable)
    - [ ]  A testing guide for reviewers
    - [ ]  A brief summary of the changes
    - [ ]  Follow the MC official PR template (https://sites.google.com/mangochango.com/knowledge-repository/templates-presentations/pr-template)
- [ ]  Update API documentation (Swagger, OpenAPI, README) if applicable.
- [ ]  Ensure user-facing documentation is updated if necessary.

## CI/CD and Deployment

- [ ]  Confirm a successful build in the CI/CD pipeline.
- [ ]  Ensure no secrets or sensitive information (e.g., API keys, credentials) are committed.

## Final Steps

- [ ]  Review **commit messages** for clarity and adherence to guidelines (e.g., Conventional Commits: `feat:`, `fix:`, `chore:`).
- [ ]  Perform a final diff check to ensure only intended changes are included.
- [ ]  Assign appropriate code reviewers.
