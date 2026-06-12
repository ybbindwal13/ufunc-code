For this authentication-related change, I would include only the files that provide the necessary implementation context while avoiding unnecessary exposure of sensitive information.
Files to include using @ mentions:
Authentication service files that handle login, logout, token generation, and validation.
Relevant API endpoint or controller files that interact with authentication.
User model or schema definitions needed to understand authentication flows.
Configuration files that define authentication settings (with secrets, API keys, and credentials redacted).
Existing unit or integration tests related to authentication.
Project documentation explaining the authentication architecture.
Files to exclude:
Production databases or data exports containing user information.
Files containing API keys, passwords, tokens, certificates, or secrets.
Unrelated modules that do not affect authentication.
Logs containing user activity or personally identifiable information (PII).
This approach gives Claude Code enough context to understand the authentication workflow and make accurate code changes while maintaining security, privacy, and the principle of least privilege.
