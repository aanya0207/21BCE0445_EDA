 🧠 Exploratory Data Analysis (EDA) on PhD Publications Dataset

👩‍💻 Author: [Aanya Kumar (21BCE0445)](https://github.com/aanya0207/21BCE0445_EDA)  
🔗 Project Link: [GitHub Repository](https://github.com/aanya0207/21BCE0445_EDA)  
📘 Open in Colab: [Run the Notebook](https://colab.research.google.com/github/aanya0207/21BCE0445_EDA/blob/main/EDA.ipynb)


💡 What is this Project?
This project performs Exploratory Data Analysis (EDA) on a dataset named `PhDPublications.csv`, which contains information about PhD candidates — including their **number of publications, gender, marital status, number of kids, mentor prestige, and mentorship details.
The goal is to explore, clean, and visualize the data to uncover **hidden trends, patterns, and relationships** that influence publication output among PhD scholars.



🎯 Why this Project?
Understanding academic publication patterns helps answer key questions like:
- Do **marital status** or number of kids affect research productivity?
- Does a **prestigious mentor** correlate with more publications?
- Are there gender-based publication differences?
- What are the **outliers or unusual cases** in the dataset?

By answering these, the project demonstrates:
- Strong command over **data wrangling, transformation, and visualization**.
- Ability to derive **data-driven insights**.
- Real-world application of **EDA for decision-making and hypothesis generation**.



⚙️ How it was Done

1️⃣ Data Understanding
Dataset:`PhDPublications.csv`  
Columns:
- `articles`: Number of academic publications  
- `gender`: Male/Female  
- `married`: Marital status  
- `kids`: Number of children  
- `prestige`: Mentor prestige score  
- `mentor`: Mentor count  

2️⃣ Data Preprocessing
- Checked for missing values → none found.  
- Removed duplicates and reset index.  
- Renamed columns (e.g., `articles → publications`) for clarity.  
- Converted data types where necessary.


3️⃣ Feature Engineering
- Added `family_size = kids + 2`  
- Normalized `prestige` using **Min–Max scaling**  
- Created **binned categories**:
  - `publications_binned` → Low / Medium / High  
  - `prestige_binned` → Very Low / Low / High / Very High  
  - `kids_binned` → No Kids / Few / Some / Many  
These transformations simplified analysis and improved interpretability.

4️⃣ Outlier Detection
Applied two statistical techniques:
- IQR Method: Removed extreme values beyond 1.5×IQR in `publications` and `kids`.  
- Z-Score Method: Filtered rows where |Z| > 3 for standardized publication counts.  
This ensured that visualizations reflected meaningful patterns, not skewed data.

5️⃣ Data Analysis
Conducted three levels of analysis:
🔹 Univariate Analysis
- Histograms and KDE plots to study single variable distributions (e.g., `publications`, `prestige`).
🔹 Bivariate Analysis
- Scatter plots (e.g., `publications` vs `kids`) to observe relationships.
- Grouped averages by gender and marital status.
🔹 Multivariate Analysis
- Pair plots and heatmaps to visualize correlations between numerical columns.

6️⃣ Visualization Techniques
Used:
- Seaborn for heatmaps, pairplots, and boxplots.  
- Matplotlib for histograms and bar charts.  
These helped in visually summarizing relationships and trends across the dataset.

🧩 Tools & Libraries
```python
pandas, numpy, matplotlib, seaborn, scipy
