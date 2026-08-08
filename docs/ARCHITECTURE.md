# FinShield Architecture

FinShield unifies loan underwriting and insurance analysis in one explainable workflow. Applicants submit financial information and documents; the system prepares structured insights and recommendations for human reviewers.

```text
User
  -> React frontend (Vite + JSX)
  -> document upload and HTTP API requests
  -> backend API server
       -> document parser
       -> NVIDIA AI analysis
       -> business logic
  -> risk assessment engine
       -> credit analysis
       -> fraud detection
       -> insurance analysis
  -> recommendation generator
  -> dashboard and explainable report
```

The frontend uses React, JavaScript/JSX, and CSS, with Vite for tooling. Tests use Vitest and React Testing Library. AI services must remain separate from UI code, use environment-based credentials, and return validated structured data.

The system provides decision support rather than autonomous approval: a human reviewer makes the final lending or insurance decision.
