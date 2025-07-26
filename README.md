# Global Climate Change Analysis 🌍📈🌡️

This project aims to analyze various global climate indicators, including **surface temperature, atmospheric CO₂ concentrations, forest area, and climate-related disaster frequency**. It visualizes trends, examines correlations between these indicators, and highlights significant changes over time using Python.

## Project Description ✨

This analysis processes and visualizes four key climate datasets to understand the complex interplay of factors contributing to global climate change.

The project performs:
* **Data Ingestion and Preprocessing:** Reads and cleans data from multiple CSV files, handling missing values and extracting relevant columns. 🧹
* **Data Alignment:** Aligns all datasets to a common set of years to enable synchronized trend analysis and correlation studies. 🔗
* **Trend Analysis:** Visualizes individual and combined trends of temperature, CO₂, forest area, and disaster frequency over time. 📊
* **Relationship Exploration:** Uses scatter plots to show relationships between indicators (e.g., CO₂ vs. Temperature), including regression lines and R-squared values. 🔍
* **Change Analysis:** Calculates and visualizes year-over-year percentage changes and total percentage changes from the first to the last year for each indicator. 💹
* **Correlation Analysis:** Computes and visualizes the correlation matrix between all indicators to identify strong relationships. 🤝

## Full Project Process ⚙️

The project follows a standard data analysis pipeline, starting from raw data and culminating in visual insights and correlational understanding of various climate indicators.

### 1. Project Setup and Environment Configuration 💻
* **Goal:** Prepare the local environment to run the analysis.
* **Steps:**
    * **Repository Cloning/Setup:** The project files (the Jupyter Notebook and the CSV datasets) are obtained, either by cloning a Git repository from GitHub or by directly downloading them to a local directory.
    * **Python Installation:** Ensure a compatible version of Python (e.g., Python 3.x) is installed on the system.
    * **Library Installation:** Install necessary Python libraries such as `numpy` for numerical operations and `matplotlib` for plotting. These are typically installed using `pip`.
    * **Jupyter Notebook Setup:** Install and launch Jupyter Notebook, which provides an interactive environment to run the Python code and display visualizations directly.
* **Tools:** Git, Python, pip, Jupyter Notebook.

### 2. Data Acquisition (Input Data) 📥
* **Goal:** Obtain the raw data needed for the analysis.
* **Steps:**
    * The project relies on four specific CSV files, which are assumed to be present in the same directory as the Jupyter Notebook. These files contain data on:
        * Global Surface Temperature
        * Monthly Atmospheric Carbon Dioxide (CO₂) concentrations
        * Forest Area
        * Climate-related Disaster Frequencies
* **Tools:** CSV files.

### 3. Data Loading and Initial Preprocessing 🧹📊
* **Goal:** Read the raw data from CSV files into Python and perform initial cleaning.
* **Steps:**
    * **Helper Function:** A `read_csv` helper function is defined to standardize the reading of CSV files, returning data as a list of lists.
    * **Individual Data Loading:** Each of the four CSV files is loaded sequentially.
    * **Header and Data Separation:** For each dataset, the header row is separated from the actual data rows.
    * **Column Selection and Type Conversion:** Specific columns representing years and their corresponding values are extracted and converted to `float` or `int`. Missing values are handled as `np.nan`. Aggregation (e.g., calculating global means or sums) is performed as needed for each indicator.
* **Tools:** Python's built-in `csv` module, `numpy` (`np.nan`, `np.nanmean`, `np.nansum`).

### 4. Data Alignment 📏
* **Goal:** Ensure all datasets cover a common time period for synchronized analysis.
* **Steps:**
    * **Identify Common Years:** The project finds the intersection of years present in all four datasets to determine the `common_years`.
    * **Alignment Function:** A helper function `align_data` is created to align each dataset to these `common_years`, inserting `np.nan` for missing years.
    * **Apply Alignment:** Each of the four processed datasets (temperature, CO₂, forest, disasters) is aligned to these `common_years`.
* **Tools:** Python `set` operations, `numpy`.

### 5. Correlation Analysis ↔️
* **Goal:** Quantify the linear relationships between the different climate indicators.
* **Steps:**
    * **Data Matrix Creation:** The aligned data for temperature, CO₂, forest, and disasters is stacked vertically to form a single data matrix.
    * **Correlation Matrix Calculation:** `np.corrcoef` is used on this data matrix to compute the pairwise Pearson correlation coefficients between all indicators.
* **Tools:** `numpy` (`np.vstack`, `np.corrcoef`).

### 6. Visualization and Insights Generation 📈📉
* **Goal:** Present the analysis findings through various plots and graphical representations.
* **Steps:**
    * **Global Styling:** Matplotlib's default style and global `rcParams` are updated for consistent plot aesthetics.
    * **Plot Generation:** Eleven distinct plots are generated, covering combined trends, individual trends with regression, scatter plots with correlation, year-over-year changes, overall percentage changes, and a correlation heatmap.
* **Tools:** `matplotlib.pyplot`, `numpy` (for `diff`, `polyfit`, `corrcoef`).

### 7. Interpretation and Documentation ✍️
* **Goal:** Summarize findings and provide instructions for project use.
* **Steps:**
    * **README.md Generation:** A `README.md` file is created to describe the project, its features, technologies, installation steps, usage instructions, and a detailed list of the visualizations generated.
    * **Analysis of Results:** The generated plots and correlation matrix are interpreted to draw conclusions about climate change trends and the relationships between various indicators.
* **Tools:** Markdown, human analysis.

## Datasets Used 📁

The analysis relies on the following CSV files, which are expected to be in the same directory as the notebook:

* `Indicator_3_1_Climate_Indicators_Annual_Mean_Global_Surface_Temperature_577579683071085080.csv` (for Temperature Data) 🌡️
* `Indicator_3_2_Climate_Indicators_Monthly_Atmospheric_Carbon_Dioxide_concentrations_-7117330003911643847.csv` (for CO₂ Data) 💨
* `Forest_and_Carbon.csv` (for Forest Data) 🌳
* `Indicator_11_1_Physical_Risks_Climate_related_disasters_frequency_7212563912390016675.csv` (for Disaster Data) 🌪️

**(Note: Please ensure these CSV files are present in your project directory or provide instructions on how to obtain them.)**

## Technologies Used 🛠️

* **Python 3.x** 🐍
* **NumPy:** For numerical operations and array manipulation.
* **Matplotlib:** For creating static, animated, and interactive visualizations.
* **CSV Module:** For reading CSV files.

## Installation 🚀

To set up and run this project, follow these steps:

1.  **Clone the repository** (if it's hosted on GitHub):
    ```bash
    git clone [https://github.com/hackeR200364/Global-Climate-Change-Analysis.git](https://github.com/hackeR200364/Global-Climate-Change-Analysis.git)
    cd Global-Climate-Change-Analysis
    ```
    If you received the files directly, just navigate to the project directory.

2.  **Ensure you have Python installed.** If not, download it from [python.org](https://www.python.org/).

3.  **Install the required Python libraries:**
    ```bash
    pip install numpy matplotlib
    ```

4.  **Place the dataset CSV files** in the project directory alongside the notebook.

## Usage ▶️

To run the analysis and generate the visualizations:

1.  Open the Jupyter Notebook:
    ```bash
    jupyter notebook
    ```
    (If you don't have Jupyter Notebook installed, you can install it via `pip install notebook`.)

2.  Navigate to the `Global_Climate_Change_Analysis.ipynb` (or similar name if you renamed it) file and open it.

3.  Run all cells in the notebook. The script will process the data and display various plots.

## Graphs/Visualizations 📊🖼️

The notebook generates **11 distinct visualizations** to illustrate the climate data. Each plot provides unique insights into the trends and relationships between different climate indicators.

### 1. Combined Trend (All Indicators)
A multi-axis plot showing global temperature, CO₂ concentration, forest area, and climate-related disaster frequency over common years. This allows for a quick visual comparison of trends across different indicators. 📈
![Climate Indicators Over Time (Aligned Years)](Climate%20Indicators%20Over%20Time%20(Aligned%20Years).png)

### 2. Global Temperature Over Time
A line plot displaying the trend of global surface temperature over the common years, including a linear regression trend line. 🌡️➡️📈
![Global Temperature Over Time](Global%20Temperature%20Over%20Time.png)

### 3. Atmospheric CO₂ Over Time
A line plot illustrating the trend of atmospheric carbon dioxide concentrations over the common years, including a linear regression trend line. 💨➡️📈
![Atmospheric CO2 Over Time](Atmospheric%20CO2%20Over%20Time.png)

### 4. Global Forest Area Over Time
A line plot showing the trend of global forest area (in million units) over the common years, including a linear regression trend line. 🌳➡️📉
![Global Forest Area Over Time](Global%20Forest%20Area%20Over%20Time.png)

### 5. Climate-related Disasters Over Time
A line plot depicting the frequency of climate-related disasters over the common years, including a linear regression trend line. 🌪️➡️📈
![Climate-Related Disasters Over Time](Climate-Related%20Disasters%20Over%20Time.png)

### 6. CO₂ vs Temperature (Scatter Plot)
A scatter plot showing the relationship between CO₂ concentrations and global temperature, with a linear regression line and R-squared value to indicate correlation strength. 🌡️vs💨
![CO2 vs Temperature](CO2%20vs%20Temperature.png)

### 7. Forest vs Temperature (Scatter Plot)
A scatter plot illustrating the relationship between global forest area and global temperature, with a linear regression line and R-squared value. 🌳vs🌡️
![Forest vs Temperature](Forest%20vs%20Temperature.png)

### 8. Disasters vs Temperature (Scatter Plot)
A scatter plot demonstrating the relationship between the frequency of climate-related disasters and global temperature, with a linear regression line and R-squared value. 🌪️vs🌡️
![Disasters vs Temperature](Disasters%20vs%20Temperature.png)

### 9. Year-over-Year Percentage Change
A line plot showing the annual percentage change for temperature, CO₂, forest area, and disasters, providing insight into the rate of change for each indicator. 💹📈📉
![Year Over Year Percentage Change](Year%20Over%20Year%20Percentage%20Change.png)

### 10. Percentage Change (First vs Last Year)
A bar chart visualizing the total percentage change for each indicator from the first common year to the last, offering an overall summary of change. 📊⬆️⬇️
![Percentage Change (First vs Last Year)](Percentage%20Change%20(First%20vs%20Last%20Year).png)

### 11. Correlation Matrix of Climate Indicators (Heatmap)
A heatmap displaying the correlation coefficients between all pairs of the four climate indicators (Temperature, CO₂, Forest, Disasters), with values annotated for easy interpretation. 🔗📊
![Correlation Matrix of Climate Indicators](Correlation%20Matrix%20of%20Climate%20Indicators.png)

## Contributing 🙏

Feel free to contribute to this project by:

* Suggesting new analysis techniques or visualizations. 💡
* Improving data cleaning or processing steps. 🛠️
* Adding more climate indicators. ➕
* Reporting bugs or suggesting enhancements. 🐛
