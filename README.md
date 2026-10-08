# Singapore Graduate Career Outcomes

## Project Overview

This project analyses graduate career outcomes in Singapore using graduate employment, salary, benefits, employment-rate, and working-hours data. It explores how degree choice and gender relate to expected career outcomes and combines Python-based data analysis with a UiPath automation workflow for processing and sharing the results.

## Research Question

**What career outcomes can graduates expect in Singapore, based on their degree choice and gender?**

The analysis focuses on three supporting questions:

1. How do different degrees influence salary outcomes and extra benefits?
2. How does gender affect employment rates?
3. How does gender shape work-life balance through differences in working hours?

## Repository Files

| File or folder | Description |
|---|---|
| [CA2 Draft.ipynb](CA2%20Draft.ipynb) | Jupyter Notebook containing data preparation, analysis, visualisations, reflections, and conclusions |
| [CA2 Datasets](CA2%20Datasets/) | Source CSV and Excel datasets used in the analysis |
| [Automation](Automation/) | UiPath Studio project for automating file preparation, Python execution, and email delivery |
| [PDAS_CA2_presentation.pptx](PDAS_CA2_presentation.pptx) | Presentation summarising the project and its findings |

## Dataset Files

- `(1) graduate employment survey modified.csv`
- `(2) graduate employment survey modified .csv`
- `Copy of LFR2023_SectionF.xlsx`
- `EmploymentRateofResidentsAged25to64bySex.csv`

The datasets contain graduate employment and salary records together with labour-force indicators by gender. They are included for reproducibility and portfolio review.

## Project Workflow

1. Import the CSV and Excel source files.
2. Convert relevant columns from text to numeric values.
3. Reformat the labour-force tables and remove blank rows and columns.
4. Merge the graduate employment datasets using their shared key columns.
5. Remove duplicate data and review outliers.
6. Scale the year values and normalise degree names into consistent groups.
7. Analyse salary, benefits, working hours, employment trends, and relationships between variables.
8. Visualise the results and document the main conclusions.
9. Use UiPath to support the file-processing and result-delivery workflow.

## Analysis and Visualisations

The notebook includes:

- Salary distribution by degree group
- Average extra benefits by degree group
- Distribution of weekly working hours
- Average weekly working hours by gender
- Employment-rate trends by gender from 2013 to 2022
- Relationships between employment rate, salary, and extra benefits

## Key Findings

- Law, Dentistry, and Double Degree graduates recorded the highest salaries, while Hospitality and Tourism recorded the lowest. The overall monthly salary average in the analysed data was approximately **SGD 3,500**.
- Medicine, Law, and Health Sciences recorded the highest extra benefits, at more than **SGD 150 per month**. The overall monthly benefit average was approximately **SGD 100**.
- Male employment rates remained around **88–90%**, while female employment rates increased from approximately **69% in 2013** to more than **76% in 2022**.
- Average weekly working hours were approximately **45 hours for men** and **41 hours for women**, with an overall average of **43 hours** and a downward trend over time.
- Employment rate and salary showed a positive relationship, as did salary and extra benefits. The relationship between employment rate and benefits was comparatively weak.

These findings describe patterns in the supplied datasets and should not be interpreted as proof of causation.

## UiPath Automation

The [Automation](Automation/) folder contains the UiPath project files, including `Main.xaml`, `project.json`, and `project.uiproj`. The workflow was designed to prepare the source data, run the Python analysis, and send the results through Outlook.

Before running the automation:

- Open the project in UiPath Studio and restore its dependencies.
- Replace the local Windows paths in `Main.xaml` with paths on your computer.
- Update the Python script path used by the workflow. The repository provides the analysis as a Jupyter Notebook, while the original automation references a local Python script.
- Set the intended email recipient and confirm the attachment paths.
- Ensure Microsoft Excel, Outlook, Python, and the required UiPath packages are available.

## Tools Used

- Python
- pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
- Microsoft Excel
- UiPath Studio
- Microsoft Outlook

## How to Run the Analysis

1. Clone or download this repository.
2. Install the Python dependencies:

   ```bash
   pip install pandas numpy matplotlib seaborn openpyxl notebook
   ```

3. Open `CA2 Draft.ipynb` in Jupyter Notebook or JupyterLab.
4. Update any local dataset paths in the notebook so they point to the `CA2 Datasets` folder.
5. Run the notebook cells in order.

## Limitations and Future Improvements

- Some notebook and UiPath file references use local Windows paths and must be updated before the project can run on another computer.
- The UiPath workflow references an original local Python script that is not included; it can be adapted to execute an exported version of the notebook instead.
- The analysis is limited to the available years, variables, and degree classifications in the supplied datasets.
- Future work could add interactive dashboards, more recent data, statistical significance testing, and a fully portable end-to-end automation workflow.

## Author

**Yan Myoe Naing**<br>
Applied AI and Analytics, Singapore Polytechnic
