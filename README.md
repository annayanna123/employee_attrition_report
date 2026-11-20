# Employee Attrition Report

This project contains a Microsoft Power BI report for analyzing employee attrition. It combines workforce information with interactive visuals to help compare attrition patterns across departments, salary bands, age ranges, overtime status, gender, and job satisfaction.

## Report overview

The report includes:

- Department-level headcount and exit analysis
- Attrition rate by department
- Attrition rate by salary band
- Attrition rate by age range
- Attrition by overtime status
- Gender and job satisfaction filters
- A department with the highest attrition percentage
- Drill-through filtering by job role

The semantic model provides the following key measures:

| Measure | Description |
|---|---|
| `Headcount` | Count of employee records |
| `Exits` | Employees whose attrition flag is `Yes` |
| `Attrition Rate` | Exits divided by headcount |
| `Worst Department` | Department with the highest attrition rate |

## Project structure

```text
employee_attrition_report/
├── employee_attrition.pbip
├── employee_attrition.Report/
│   └── definition/
│       ├── report.json
│       └── pages/
└── employee_attrition.SemanticModel/
    └── definition/
        ├── model.tmdl
        └── tables/hr-attrition.tmdl
```

- `employee_attrition.pbip` is the Power BI Project entry point.
- `employee_attrition.Report` contains the report pages and visual definitions.
- `employee_attrition.SemanticModel` contains the imported data model, measures, columns, relationships, and table calculations.

## Data source

The semantic model imports data from a CSV file configured in `hr-attrition.tmdl`.
To open or refresh the report on another machine, update the `Source` step in the `hr-attrition` Power Query partition to point to the local HR attrition CSV.

### Expected fields

The CSV is expected to contain:

- `employee_id`
- `department`
- `job_role`
- `hire_date`
- `exit_date`
- `monthly_salary`
- `age`
- `gender`
- `regular_overtime`
- `job_satisfaction`

The model derives `attrition_flag`, `salary_band`, and `age_range` during data transformation.

## Open the report

1. Install Microsoft Power BI Desktop.
2. Clone or download this repository.
3. Open `employee_attrition.pbip` in Power BI Desktop.
4. If prompted, update the CSV file path and refresh the semantic model.

Power BI Desktop may require one or more refresh prompts for the first local update.
