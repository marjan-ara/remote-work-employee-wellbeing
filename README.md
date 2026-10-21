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

The editable Power BI dashboard is available at:

`dashboard/dashboard.pbix`

Open this file using Power BI Desktop.

**Note:** Power BI Desktop requires Windows. macOS users can review an exported PDF of the dashboard if one is provided.

### 6. Verify the Results

The notebook reproduces the descriptive statistics and statistical analysis supporting the Power BI dashboard.

Expected results include:

- Total respondents: 3,157
- Overall high-burnout rate: 33.1%
- Highest high-burnout rate: Remote (46.43%)
- Chi-square statistic: 117.85
- Cramer's V: 0.137

These results should be reproducible using the included dataset and dependencies.