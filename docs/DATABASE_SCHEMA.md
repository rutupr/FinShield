# Database Schema

## Customer

| Field | Type | Description |
| --- | --- | --- |
| CustomerID | UUID | Unique customer identifier |
| FullName | String | Customer name |
| MobileNumber | String | Contact number |
| DateOfBirth | Date | Date of birth |

## LoanApplication

| Field | Type | Description |
| --- | --- | --- |
| ApplicationID | UUID | Unique application identifier |
| CustomerID | UUID | Customer reference |
| RequestedLoanAmount | Decimal | Requested amount |
| MonthlySalary | Decimal | Monthly net salary |
| CurrentEMI | Decimal | Existing monthly EMI |
| ApplicationStatus | Enum | Pending, Approved, Rejected, or Under Review |

## FinancialDocument

| Field | Type | Description |
| --- | --- | --- |
| DocumentID | UUID | Unique document identifier |
| ApplicationID | UUID | Application reference |
| DocumentType | Enum | Income Certificate, Salary Slip, Bank Statement, or Credit Report |
| FileName | String | Uploaded file name |
| UploadTimestamp | Timestamp | Upload time |
| ProcessingStatus | Enum | Uploaded, Processing, or Completed |

## AIAnalysis

Includes `AnalysisID`, `ApplicationID`, extracted income and EMI, insurance coverage, fraud indicators, and a confidence score.

## RiskAssessment

Includes `RiskID`, `ApplicationID`, income stability, insurance adequacy, fraud signal, default probability, and an overall score from 0 to 100.

## RecommendationReport

Includes `RecommendationID`, `ApplicationID`, an Approve/Review/Reject recommendation, suggested loan amount, insurance recommendation, and an explainable rationale.
