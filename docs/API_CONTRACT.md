# API Contract

> The current repository is a frontend prototype. These endpoints define the intended backend contract.

## `POST /api/applications`

Creates a loan application.

Request fields: `fullName`, `mobileNumber`, `dateOfBirth`, `requestedLoanAmount`, `monthlySalary`, and `currentEmi`.

Response: `{ "applicationId": "uuid", "status": "Pending" }`.

## `POST /api/applications/{applicationId}/documents`

Uploads an income certificate, salary slip, bank statement, credit report, or insurance policy. Accept multipart form data with `documentType` and `file`.

Response: `{ "documentId": "uuid", "processingStatus": "Uploaded" }`.

## `POST /api/applications/{applicationId}/analyze`

Starts structured document and risk analysis.

Response: `{ "analysisId": "uuid", "status": "Processing" }`.

## `GET /api/applications/{applicationId}/report`

Returns the decision-support report, including extracted financial data, risk indicators, recommendation, and explanation. A report recommendation is advisory; human approval is required.

## Error format

Use `{ "error": { "code": "VALIDATION_ERROR", "message": "..." } }` with appropriate HTTP status codes. Never include credentials or raw sensitive document content in error messages.
