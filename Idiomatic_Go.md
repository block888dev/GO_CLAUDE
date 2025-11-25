✅ Go Project Rules (Idiomatic Go)

### CI & Workflow

All CI workflows must pass before code changes may be reviewed.

The existing project structure must not be changed without a strong reason.

Every change must be covered by automated tests.

README.md must explain the repository’s purpose clearly and concisely, and be free of typos or bad grammar.

### Code Style & Structure

All code must be formatted using gofmt and goimports.

Package names must be short, lowercase, and meaningful.

Avoid global state; use dependency injection or explicit parameters.

Avoid unnecessary interfaces. Create an interface only when it is consumed by multiple implementations or needed for testing.

Prefer returning concrete types; accept interfaces.

Keep functions small and cohesive.

Function names must be descriptive and follow Go naming conventions; compound names are allowed.

Avoid overly complex type hierarchies; prefer composition over inheritance (Go has no inheritance).

Constructors (NewX) may perform validation and return errors.

Exported types and functions must have proper GoDoc comments.

Error messages must not end with a period.

Errors must include contextual information using fmt.Errorf("...: %w", err).

###Testing

Every bug must be covered by a test that reproduces the issue before fixing it.

Every new feature must include tests before merging.

Tests must not rely on external services or the Internet.

Tests must use timeouts when waiting for events.

Tests must close all opened resources (files, connections).

Table-driven tests are encouraged.

Tests should use random inputs when reasonable.

Tests should not rely on global state or shared mutable resources.

Tests must use temporary directories for temporary files (t.TempDir()).

Tests must not wait indefinitely; all goroutine coordination must use timeouts.

Tests should not assert on logging output.

Each test should verify exactly one behavior or scenario.
