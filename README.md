 Project Cost Analysis Tool
A Python tool for construction project cost monitoring in a structural engineering context.

What It Does
Loads site-level project data from a .csv file

Calculates total cost per site (materials + labour)

Compares actual vs. estimated cost and duration

Flags sites with cost overruns or schedule delays

Forecasts cost at completion if delay trends continue

Exports results to .csv and .txt summary reports

 ## Workflow

```mermaid
flowchart TD
    A[Start] --> B[Load project_data_jupyter.csv]
    B --> C[Read site, cost and duration data]
    C --> D[Calculate estimated total cost]
    C --> E[Calculate actual total cost]
    D --> F[Compare actual vs estimated cost]
    E --> F
    C --> G[Compare actual vs planned duration]
    F --> H{Cost overrun?}
    G --> I{Schedule delay?}
    H -->|Yes| J[Flag COST OVERRUN]
    H -->|No| K[No cost flag]
    I -->|Yes| L[Flag POTENTIAL DELAY]
    I -->|No| M[No delay flag]
    J --> N[Forecast cost at completion]
    K --> N
    L --> N
    M --> N
    N --> O[Export summary to CSV and TXT]
    O --> P[End]
```
    
