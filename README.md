# Quarterly Enrollment Funnel Reporting in R

A reproducible enrollment analytics reporting workflow built in R and Quarto for graduate and accelerated degree completion programs.

This project generates a multi-dimensional quarterly enrollment report spanning the full admissions funnel:

- Prospect and inquiry generation
- Application starts
- Application submissions
- Program-level year-over-year comparisons
- Distribution analysis
- Cumulative funnel progression
- Small multiple visualizations for portfolio-wide monitoring

The reporting framework is designed for higher education enrollment management teams seeking transparent, repeatable, and accessible analytics workflows.

---

## Project Goals

This reporting system was developed to:

- Create reproducible quarterly enrollment reports
- Standardize admissions funnel analysis across programs
- Produce publication-ready visualizations with minimal manual formatting
- Support executive-level decision making
- Enable rapid year-over-year comparison workflows
- Emphasize clarity, accessibility, and simplicity in data storytelling

---

## Key Features

### Reproducible Reporting Pipeline

Built using:

- `R`
- `Quarto`
- `tidyverse`
- `ggplot2`
- `lubridate`

The report can be regenerated each quarter simply by updating CSV exports from the CRM.

---

### Multi-Dimensional Funnel Analysis

The report analyzes several layers of the enrollment funnel:

| Funnel Stage | Analysis Included |
|---|---|
| Prospects & Suspects | Lead generation trends |
| Applications Started | Cumulative progression |
| Applications Submitted | Quarterly and YoY comparisons |
| Program-Level Analysis | Portfolio segmentation |
| Distribution Analysis | Application timing behavior |
| Small Multiples | Program-by-program trend monitoring |

---

### Accessibility-First Visualization Design

Visualizations utilize:

- The **Okabe-Ito color palette** for colorblind accessibility
- `theme_tufte()` from `ggthemes`
- Minimalist chart design principles inspired by Edward Tufte
- Reduced chart junk and simplified axes/gridlines
- High-contrast categorical comparison structures

The goal is to produce visualizations that remain:

- Executive readable
- Print friendly
- Presentation ready
- Accessible to broad audiences

---

## Visualization Examples

This report includes:

- Cumulative line charts
- YoY grouped bar charts
- Histogram-based distribution analysis
- Faceted small multiples
- Program segmentation dashboards
- Funnel trend monitoring

---

## Example Outputs

### Graduate Funnel Reporting

- Application start velocity
- Program-level cumulative growth
- Submitted application comparisons
- Distribution timing analysis

### Accelerated Degree Completion Reporting

- Application progression tracking
- Concentration-level performance
- YoY application comparisons
- Funnel monitoring across adult learner programs

---

## Technical Highlights

### Dynamic Program Abbreviation Mapping

Long academic program names are programmatically abbreviated for cleaner chart rendering and improved readability.

```r
"Master's in Applied Analytics" = "MAA"
"Graduate Certificate in Applied Analytics" = "GCAA"
```

---

### Robust Date Parsing

The workflow supports multiple date formats including:

- `m/d/Y`
- ISO timestamps
- CRM-exported datetime fields

This reduces preprocessing friction when working with inconsistent exports.

---

### Modular Summarization Functions

Reusable helper functions simplify aggregation workflows:

```r
summarize_leads <- function(d, program_type) {
  ...
}
```

This structure improves maintainability and reduces duplicated code.

---

## Design Philosophy

This project follows several principles:

- Reproducibility over spreadsheet drift
- Simplicity over dashboard clutter
- Readability over excessive customization
- Accessibility as a baseline requirement
- Narrative-oriented enrollment analytics

The intent is not merely to generate charts, but to create a coherent analytical narrative around enrollment behavior.

---

## Potential Future Enhancements

Planned or possible future improvements include:

- Interactive Shiny dashboard integration
- Parameterized Quarto reporting
- Automated CRM/API ingestion
- Forecasting and predictive modeling
- Funnel conversion rate analysis
- Institutional benchmarking
- Scheduled report generation

---

## Repository Structure

```text
├── quarterly_enrollment_report.qmd
├── README.md
└── Report Screenshots
```

---

## Running the Report

Render the report with:

```r
quarto render quarterly_enrollment_report.qmd
```

Or from RStudio:

```r
library(quarto)
quarto_render("quarterly_enrollment_report.qmd")
```

---

## Packages Used

Core packages include:

```r
tidyverse
ggplot2
lubridate
ggthemes
stringr
forcats
readr
quarto
```

---

## Why This Matters

Many enrollment reporting processes remain trapped in fragmented spreadsheets and manual PowerPoint workflows.

This project demonstrates a more modern analytics approach:

- reproducible
- scalable
- accessible
- version controlled
- publication ready

It also creates a foundation for expanding enrollment analytics into more advanced reporting and predictive modeling workflows over time.

---

## Author

Todd Cooley  
Enrollment Analytics & Graduate Admissions  
Focused on reproducible reporting, higher education analytics, and accessible data visualization.
