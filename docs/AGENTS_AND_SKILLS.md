# Agents and Skills

## AI analysis responsibilities

NVIDIA AI supports FinShield by extracting document data, evaluating financial risk, highlighting fraud signals, evaluating insurance adequacy, and generating explainable recommendations. It does not make the final lending or insurance decision.

## Required behavior

- Use structured prompts and request structured output where possible.
- Validate model output before it reaches the dashboard.
- Keep AI integration independent of the UI so it can be changed safely.
- Do not expose provider credentials in frontend code.
- Route uncertain, incomplete, or suspicious results to human review.

## Review skills

When changing the platform, verify document upload handling, validation, risk indicators, recommendation explanations, and responsive dashboard presentation.
