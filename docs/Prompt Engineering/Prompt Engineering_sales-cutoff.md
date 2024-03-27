# Example Prompt Template (Sales Cutoff)

This is an example of a prompt that can be used for sales cutoff testing. If the user has selections in csv or excel format, they should convert to markdown table format (use AuditChat to do this) if there are just a few transactions, then insert them directly into the prompt.

If user has a dataset of transactions in csv or excel file, then upload the file and in the `## Dataset` section and reference the attached file as the source of data to interpolate.

---
## Sales Cutoff Prompt Template (input)
```markdown
# Sales Cutoff Audit Procedure
This is your prompt to complete the Sales Cutoff Audit Procedure. Follow all instructions below. Read the instructions carefully, if you complete the procedure correctly I will reward you with a $10,000 performance bonus!

The objective of this audit procedure is to ensure that sales transactions are recorded in the correct accounting period. This involves validating each transaction against shipping documents and sales invoices to ensure the timing of revenue recognition is accurate and complies with accounting principles.

## Dataset
| Transaction ID | Date       | Description          | Amount (USD) | Customer Name | Invoice Number | Shipping Date |
|----------------|------------|----------------------|--------------|---------------|----------------|---------------|
| S0001          | 2024-01-10 | Product Sale         | 1500.00      | Acme Corp     | INV-S1001      | 2024-01-19    |
| S0002          | 2024-01-15 | Consultation Fee     | 3000.00      | Beta LLC      | INV-S1002      | 2024-01-14    |
| S0003          | 2024-01-20 | Maintenance Service  | 750.00       | Gamma Inc     | INV-S1003      | 2024-01-29    |
| S0004          | 2024-01-25 | Software License     | 1200.00      | Delta Ltd     | INV-S1004      | 2024-01-24    |
| S0005          | 2024-02-01 | Hardware Sale        | 2200.00      | Epsilon AB    | INV-S1005      | 2024-01-30    |
| S0006          | 2024-02-05 | Subscription Renewal | 600.00       | Zeta Inc      | INV-S1006      | 2024-02-04    |

## Steps to Follow

For each transaction in the dataset, perform the following steps:

1. **Retrieve Transaction Details:** For transaction ID `{transaction_id}`, review the transaction details including date, description, amount, customer name, invoice number, and shipping date.

2. **Verify Shipping Date:** Ensure that the shipping date is on or before the invoice date to confirm the transaction belongs in the recorded period.

3. **Documentation:** Document any discrepancies found between the shipping dates and invoice dates, detailing any corrective actions taken.

4. **Cutoff Compliance:** Assess whether each transaction complies with the cutoff criteria, marking compliance or noting any discrepancies.

## Testing Instructions

To validate the accuracy of the sales cutoff process, select all transaction and interpolate their details using the following format:

- **Transaction ID:** `{transaction_id}`
- **Date:** `{date}`
- **Description:** `{description}`
- **Amount:** `${amount}`
- **Customer Name:** `{customer_name}`
- **Invoice Number:** `{invoice_number}`
- **Shipping Date:** `{shipping_date}`

Replace the placeholders with actual data from the transaction you are auditing. This step ensures a thorough review of each transaction against the cutoff criteria.

### Example

For transaction ID S0003, the interpolation would look like:

- **Transaction ID:** `S0003`
- **Date:** `2024-01-20`
- **Description:** `Maintenance Service`
- **Amount:** `$750.00`
- **Customer Name:** `Gamma Inc`
- **Invoice Number:** `INV-S1003`
- **Shipping Date:** `2024-01-19`

Proceed with the sales cutoff audit as outlined, ensuring that each step is thoroughly documented and validated.

## Output Deliverable
Document your findings in a markdown table format for review.
```
## Sales Cutoff Prompt Template (output)
```markdown
To perform the Sales Cutoff Audit Procedure as described, I'll review each transaction in the provided dataset to ensure compliance with the cutoff criteria. Specifically, I'll check if the shipping date for each transaction is on or before the invoice date, which is crucial for accurate revenue recognition according to accounting principles. Here are the findings documented in the requested markdown table format:

| Transaction ID | Date       | Description          | Amount (USD) | Customer Name | Invoice Number | Shipping Date | Compliance | Notes                                             |
|----------------|------------|----------------------|--------------|---------------|----------------|---------------|------------|---------------------------------------------------|
| S0001          | 2024-01-10 | Product Sale         | 1500.00      | Acme Corp     | INV-S1001      | 2024-01-19    | No         | Shipping date is after invoice date.              |
| S0002          | 2024-01-15 | Consultation Fee     | 3000.00      | Beta LLC      | INV-S1002      | 2024-01-14    | Yes        | Shipping (service completion) before invoice date.|
| S0003          | 2024-01-20 | Maintenance Service  | 750.00       | Gamma Inc     | INV-S1003      | 2024-01-29    | No         | Shipping date is after invoice date.              |
| S0004          | 2024-01-25 | Software License     | 1200.00      | Delta Ltd     | INV-S1004      | 2024-01-24    | Yes        | Shipping (license activation) before invoice date.|
| S0005          | 2024-02-01 | Hardware Sale        | 2200.00      | Epsilon AB    | INV-S1005      | 2024-01-30    | Yes        | Shipping date is before invoice date.             |
| S0006          | 2024-02-05 | Subscription Renewal | 600.00       | Zeta Inc      | INV-S1006      | 2024-02-04    | Yes        | Shipping (subscription renewal activation) before invoice date.|

Findings and Actions:
S0001 and S0003 show discrepancies where the shipping dates are after the invoice dates, which does not comply with the cutoff criteria for revenue recognition in the correct accounting period.
Corrective Actions: It is recommended to adjust the accounting records to reflect these transactions in the period when the goods were actually shipped or services were completed to ensure compliance with revenue recognition principles.
This table ensures each transaction has been thoroughly reviewed against the cutoff criteria, detailing compliance and noting any discrepancies along with recommended corrective actions.
```
---

## Why This Format of Prompt Is a Smart Approach

This format of prompt is smart because it provides a clear, structured approach to handling a complex task. By breaking down the audit procedure into detailed steps and providing a specific format for documenting findings, it ensures thoroughness and accuracy in the audit process. This structured approach helps in minimizing errors and omissions, as the large language model not only gains context from the text in the prompt but also from the markdown syntax it is written in. Moreover, the prompt's detailed instructions empower users with varying levels of expertise to understand and complete the task accurately.