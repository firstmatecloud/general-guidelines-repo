# General Guidelines

## Rules

### Documentation
- Comment only when necessary, focusing on explaining why something is done rather than what is done (good code should be self-explanatory).
- Every project should have a README that explains the purpose, setup, usage, and dependencies of the project. 

### Code

- Use descriptive naming of variables, functions and classes
- Avoid duplicating code by creating reusable functions or modules.
- Use asynchronous programming to handle I/O-bound operations (e.g., network requests, file operations, database queries) without blocking the main thread or process.

### Security

- Avoid hardcoding sensitive information like passwords or API keys; use environment variables or secure vaults.
- Avoid exposing sensitive information in error messages.
- Validate and sanitize all external inputs (e.g., from users, APIs, databases) to prevent injection attacks, such as SQL injection, cross-site scripting (XSS), and command injection.
- Implement strong authentication mechanisms, such as OAuth, JWT, or API keys. Always hash passwords with a strong hashing algorithm (e.g., bcrypt, Argon2).
- Graceful failure: Ensure your application handles errors gracefully without crashing or exposing the internal state.

### Testing

- Write unit tests for critical parts of your code
- Separate source code from testing code in different folders
- Tests should be triggered in a testing pipeline (e.g. triggered on the creation of a PR)
- Use mocks and stubs for external dependencies

### Logging

- Log messages should be clear and meaningful. They should provide enough context to understand the issue.
- Log messages should contain all relevant information without exposing sensitive data on info level.
