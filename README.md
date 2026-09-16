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

TM1 Rules were designed to support calculations such as:

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

## Planning Analytics Dashboard

The following concept dashboard illustrates how the financial planning model can be presented through an executive analytics experience.

![Financial Planning Dashboard](imagenMproject.png)

> This dashboard is a portfolio visualization created to demonstrate the analytical presentation of the TM1 financial planning solution.

## Testing & Validation

The model was validated through:

- General Ledger reconciliation
- Scenario testing
- Rule accuracy checks
- Performance testing
- Stakeholder validation

## Project Result

The solution reduced reporting time by approximately **30%**, improved forecasting accuracy, and enabled business users to perform planning activities faster and more reliably.

## Technologies

- IBM Planning Analytics (TM1)
- Planning Analytics Workspace (PAW)
- TurboIntegrator
- TM1 Rules & Feeders
- MDX
- Cognos Analytics

## Documentation

Additional project documentation:

- [Business Case](docs/01-business-case.md)

## Author

**Mayra Rocio Valencia**

Planning Analytics (TM1) | Data Analytics | Data Science
