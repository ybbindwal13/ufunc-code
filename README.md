# CLAUDE.md

## Project Overview
This project is a full-stack Expense Tracker application designed to help users record, categorize, analyze, and manage personal finances. The application should prioritize accuracy, performance, maintainability, security, and user experience.

## Core Features
- User authentication and authorization
- Expense and income management
- Category management
- Budget tracking
- Financial dashboards
- Reporting and analytics
- Data export functionality
- Mobile responsive design

## Technical Standards

### Code Quality
- Use TypeScript for all new code.
- Follow clean architecture principles.
- Keep functions small and focused.
- Avoid duplicate logic.
- Add meaningful comments only when necessary.
- Maintain consistent naming conventions.

### Frontend
- Use React and Next.js.
- Prefer server components when possible.
- Use reusable UI components.
- Implement loading and error states.
- Ensure accessibility compliance.

### Backend
- Validate all inputs.
- Use proper API error handling.
- Implement rate limiting where appropriate.
- Follow RESTful design principles.
- Log critical operations.

### Database
- Use normalized schema design.
- Add indexes for frequently queried fields.
- Use transactions for financial operations.
- Never store sensitive data in plain text.

### Security
- Sanitize user input.
- Prevent SQL injection.
- Prevent XSS attacks.
- Protect against CSRF.
- Encrypt sensitive information.

### Expense Rules
- Every expense must have:
  - Amount
  - Date
  - Category
  - User ID

- Amounts must be positive values.
- Future-dated expenses require confirmation.
- Deleted expenses should be soft-deleted.

### Performance
- Optimize expensive database queries.
- Implement pagination.
- Use caching when beneficial.
- Lazy load large datasets.

### Testing
- Unit tests for business logic.
- Integration tests for APIs.
- End-to-end tests for critical user flows.
- Minimum 80% test coverage.

### UI Guidelines
- Clean financial dashboard.
- Consistent spacing and typography.
- Mobile-first design.
- Fast user interactions.
- Clear success and error messages.

### Reporting
Support:
- Monthly summaries
- Category breakdowns
- Budget comparisons
- Spending trends
- Export to CSV

### AI Development Guidelines
When generating code:
1. Prioritize correctness over speed.
2. Maintain existing architecture.
3. Avoid introducing unnecessary dependencies.
4. Write production-ready code.
5. Include error handling.
6. Consider edge cases.
7. Update tests when modifying functionality.
