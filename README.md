## Reproducing the Analysis

Follow these steps to set up the project and reproduce the analysis.

### 1. Clone the Repository

```bash
git clone https://github.com/marjan-ara/remote-work-employee-wellbeing.git
cd remote-work-employee-wellbeing
```

### 2. Create a Virtual Environment

Python 3.12 is recommended.

**macOS / Linux:**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

**Windows:**

```powershell
py -3.12 -m venv .venv
.venv\Scripts\Activate.ps1
```

### 3. Install Dependencies

```bash
python -m pip install -r requirements.txt
```

This installs the Python packages required for data analysis and running the Jupyter Notebook.

### 4. Run the Notebook

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open `remote_work_analysis.ipynb`, select the virtual environment's Python kernel, and run all cells in order.

The notebook loads the dataset from:

`data/post_pandemic_remote_work_health_impact_2025.csv`

### 5. Explore the Power BI Dashboard

**View Dashboard (PDF)** — View both dashboard pages without installing Power BI.

**Download Power BI Dashboard (.pbix)** — Open the editable dashboard in Power BI Desktop.

**View Python Analysis Notebook** — Review the reproducible analysis and statistical testing.



### 6. Verify the Results

The project uses three complementary tools to support transparency, reproducibility, and independent validation:

- **Python (Pandas and SciPy):** Performs data quality checks, descriptive analysis, and statistical testing.
- **Power BI:** Visualises the findings through a two-page dashboard.
- **Microsoft Excel:** Independently validates burnout counts and percentages using a PivotTable created from the original dataset.

The Excel workbook, [burnout_validation.xlsx](burnout_validation.xlsx), contains:

- **Raw Data:** The original imported survey dataset.
- **Burnout Validation:** A PivotTable comparing `Work_Arrangement` and `Burnout_Level`, displaying counts and percentages of row totals.

#### Expected Results

| Metric | Expected Value |
|---|---|
| Total respondents | 3,157 |
| Overall high-burnout rate | 33.13% |
| Remote high-burnout rate | 46.43% (273/588) |
| Hybrid high-burnout rate | 35.75% (360/1,007) |
| Onsite high-burnout rate | 26.44% (413/1,562) |
| Chi-square statistic | 117.85 |
| Cramer's V | 0.137 |

The Excel PivotTable independently confirms the burnout counts and rates calculated in Python and presented in Power BI. The chi-square statistic and Cramer's V are reproduced using the Python notebook.

Together, these tools provide a reproducible analytical workflow and allow the key findings to be cross-checked.

