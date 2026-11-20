# AGENTS.md

Guidance for AI coding agents (Codex, Claude Code, etc.) working in **Leeway CRM**, an AI-first CRM.

## About the owner

- 20 years in technology. Strong in **SQL**, **.NET**, and **C#**. Now in a leadership role managing developers, so writes less code day to day.
- Not a front-end specialist. HTML/CSS/JavaScript is the weakest area, but picks up concepts quickly.
- Prefers clear explanations over jargon, especially for front-end work.

## How I like to work

### Explanations
- Explain the *why* behind changes, not just the *what*.
- For front-end or JavaScript changes, briefly explain the concept in plain terms. Relate it to C#/.NET or SQL when that helps (e.g. "a JS Promise is like a `Task` in C#").
- Keep summaries short and scannable: what changed, why, and anything I need to decide.

### Code style
- **Back end:** C# / .NET. Follow standard .NET conventions (PascalCase for types and methods, `async`/`await` end to end, dependency injection, nullable reference types enabled).
- **Data:** Prefer clean, readable SQL. Use parameterized queries only; never build SQL with string concatenation. Name tables, keys, and indexes clearly and consistently.
- **Front end:** Keep it simple and well commented. Avoid clever one-liners; readability beats brevity.
- Small, focused methods and classes. Favor clarity over cleverness.

### Changes and git
- Work on a feature branch off `Development`. Never commit directly to `main` or `Development`.
- Keep commits small and focused, with messages that say what changed and why.
- Don't open pull requests unless asked.
- Don't add new dependencies or packages without calling it out and explaining the reason.

### Quality
- Add or update tests for any logic change (xUnit preferred for .NET).
- Build and run tests before calling something done. If anything fails or was skipped, say so plainly.
- Never commit secrets, connection strings, or API keys. Use configuration / user secrets / environment variables.

### When unsure
- If a requirement is ambiguous or a decision has trade-offs, give a recommendation and the reasoning instead of a long list of options.
- Ask before any destructive action (dropping tables, deleting data, rewriting history).

## Project notes

- Repo: `bradpurdue/Leeway-crm`
- Branching: `main` (release), `Development` (integration), feature branches off `Development`.
- Stack: Visual Studio / .NET solution (per `.gitignore`). Update this section as the project structure takes shape.
