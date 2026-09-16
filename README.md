# IBM Planning Analytics (TM1) – Financial Planning Solution

End-to-end financial planning, budgeting, and forecasting solution developed using IBM Planning Analytics (TM1), Planning Analytics Workspace (PAW), Cognos Analytics, and TurboIntegrator.

## Project Overview

The objective of this project was to modernize the financial planning, budgeting, and forecasting process through a multidimensional TM1 model.

My responsibilities included:

- TM1 model design
- Dimension and hierarchy development
- Cube development
- TurboIntegrator automation
- Business Rules and Feeders
- Performance optimization
- Data validation
- Reporting and dashboards
- Documentation

## Solution Architecture

```text
Source Data
    │
    ▼
TurboIntegrator
    │
    ▼
Dimensions & Hierarchies
    │
    ▼
TM1 Cubes
    │
    ▼
Rules & Feeders
    │
    ▼
MDX / Views
    │
    ▼
PAW / Cognos Analytics
```

## Financial Planning Model

The solution includes financial planning and reporting components for:

- OPEX
- Budget
- Forecast
- Workforce Planning
- General Ledger validation

The multidimensional model includes dimensions such as:

- Account
- Cost Center
- Product
- Time
- Version
- Measures
- Currency

## Rules & Feeders

TM1 Rules were designed to support business calculations including:

- Allocation logic
- Salary calculations
- OPEX spreading
- Currency conversion
- Actual vs Budget vs Forecast variance analysis

Feeders were implemented to support calculation performance and reduce unnecessary overfeeding.

## TurboIntegrator

TurboIntegrator processes were developed to automate:

- General Ledger data loading
- Dimension updates
- Actual data loading
- Budget loading
- Forecast loading
- Data cleansing and validation
- Cube exports for reporting
- Scheduled processing through chores

The automation process also included error handling, logging, checkpoints, and audit controls.

## Planning Analytics Dashboard

The following concept dashboard illustrates how the financial planning model can be presented through an executive analytics experience.

![Financial Planning Dashboard](imageMproject.png)

> **Portfolio Visualization:** This dashboard was created to demonstrate the analytical presentation of the TM1 financial planning solution.

## Planning Analytics Workspace

The reporting solution includes analytical components such as:

- Executive summary reports
- Trend analysis
- Variance analysis
- Budget and Forecast input forms
- KPI visualization
- Conditional formatting

## Testing & Validation

The TM1 model was validated through:

- General Ledger reconciliation
- Scenario testing
- Rule accuracy checks
- Performance testing
- Stakeholder validation

## Project Results

The solution reduced reporting time by approximately **30%**, improved forecasting accuracy, and enabled business users to perform planning activities faster and more reliably.

## Technologies

- IBM Planning Analytics (TM1)
- Planning Analytics Workspace (PAW)
- TurboIntegrator
- TM1 Rules & Feeders
- MDX
- Cognos Analytics

## Documentation

Additional project documentation is available in this repository:

- [Business Case](docs/01-business-case.md)

## Author

**Mayra Rocio Valencia**

Planning Analytics (TM1) | Data Analytics | Data Science
