# FinShield Agent Guidelines

## Scope

FinShield is an explainable decision-support platform for loan underwriting and insurance analysis. AI assists reviewers; a human makes the final decision.

## Development principles

- Preserve existing functionality unless a change is explicitly requested.
- Prefer small, targeted changes and reuse existing components and utilities.
- Keep UI, application logic, AI services, and data handling separated.
- Keep the React, JavaScript/JSX, CSS, Vite, Vitest, and React Testing Library stack.
- Keep UI spacing, typography, controls, and responsive behavior consistent.

## Security

- Never hardcode credentials or API keys.
- Use environment variables for sensitive configuration.
- Send only information necessary for AI analysis.
- Validate incomplete or unexpected AI responses before showing them to users.
