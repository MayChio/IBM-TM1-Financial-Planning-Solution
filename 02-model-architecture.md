# TM1 Model Architecture

## Overview

This document describes the architecture of the financial planning, budgeting, and forecasting solution developed using IBM Planning Analytics (TM1).

The solution integrates source financial data, TurboIntegrator automation, multidimensional structures, business calculations, and analytical reporting.

## Architecture

```mermaid
flowchart TD

    A[Source Financial Data] --> B[TurboIntegrator]

    B --> C[Dimensions & Hierarchies]
    B --> D[TM1 Cubes]

    C --> D

    D --> E[TM1 Rules]
    E --> F[Feeders]

    D --> G[Planning & Reporting]

    G --> H[Planning Analytics Workspace]
    G --> I[Cognos Analytics]

    H --> J[Executive Reports]
    H --> K[Budget & Forecast Input]
    H --> L[Variance Analysis]

    I --> M[Financial Reporting]
```

## Data Flow

The overall data flow follows this process:

```text
Source Data
     │
     ▼
TurboIntegrator
     │
     ├── Data Validation
     ├── Data Cleansing
     ├── Dimension Updates
     └── Fact Data Loading
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
Planning & Reporting
     │
     ├── Planning Analytics Workspace
     └── Cognos Analytics
```

## Core Cubes

The solution includes multiple cubes designed for different financial planning activities.

| Cube | Purpose |
|------|---------|
| OPEX | Operating expense planning and analysis |
| Budget | Annual financial planning |
| Forecast | Monthly financial projections |
| Workforce | Salary, benefits, and headcount planning |
| GL | Validated General Ledger financial information |

## Dimensions

The multidimensional model includes the following core dimensions:

| Dimension | Purpose |
|-----------|---------|
| Account | Financial accounts and reporting structures |
| Cost Center | Business units and departments |
| Product | Product categories and subcategories |
| Time | Year, Quarter, Month, and Day |
| Version | Actual, Budget, and Forecast |
| Measures | Financial measures and KPIs |
| Currency | Currency reporting and conversion |

## Dimension Hierarchies

Example Time hierarchy:

```text
Year
└── Quarter
    └── Month
        └── Day
```

Example Version structure:

```text
Version
├── Actual
├── Budget
└── Forecast
```

Alternate hierarchies can also be used to provide additional reporting flexibility.

## TurboIntegrator Layer

TurboIntegrator processes automate the movement and preparation of data within the TM1 environment.

Processes include:

- General Ledger data loading
- Actual data loading
- Budget data loading
- Forecast data loading
- Dimension maintenance
- Data cleansing
- Data validation
- Cube exports
- Scheduled processing through chores

The automation layer also incorporates:

- Error handling
- Logging
- Checkpoints
- Audit trails

## Business Logic

TM1 Rules provide the calculation layer of the model.

Business logic includes:

- Allocation calculations
- Salary calculations
- OPEX spreading
- Currency conversion
- Actual vs Budget variance
- Actual vs Forecast variance
- Budget vs Forecast analysis

## Feeders

Feeders support rule-based calculations in sparse cubes and help improve calculation performance.

Their purpose within the architecture is to ensure that calculated cells are correctly identified while reducing unnecessary overfeeding.

## Reporting Layer

### Planning Analytics Workspace

Planning Analytics Workspace supports interactive planning and analytical experiences such as:

- Executive summary reporting
- Trend analysis
- Variance analysis
- Budget input
- Forecast input
- KPI visualization
- Conditional formatting

### Cognos Analytics

Cognos Analytics provides an additional reporting and visualization layer for financial analysis.

## Validation

The model architecture includes validation procedures such as:

- General Ledger reconciliation
- Scenario testing
- Rule accuracy checks
- Performance testing
- Stakeholder validation

## Architecture Objective

The architecture was designed to create a structured financial planning environment where data can move from source systems through automated TM1 processes into multidimensional models and ultimately into planning and analytical reporting.

The solution reduced reporting time by approximately **30%** while improving the speed and reliability of the planning process.

---

**Author:** Mayra Rocio Valencia  
**Technology:** IBM Planning Analytics (TM1)
