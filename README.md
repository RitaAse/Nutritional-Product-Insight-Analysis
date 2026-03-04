# Nutritional-Product-Insight-Analysis

## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Dataset Characteristics](#dataset-characteristics)
- [Tools](#tools)
- [Data Preparation](#data-preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Personalized Insights](#personalized-insights)
- [Implementation](#implementation)
- [Results](#results)
- [Business Impact](#business-impact)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)


### Project Overview
---
This project analyzes fruit nutritional data to uncover patterns that support product development and marketing decisions. The analysis seeks to improve understanding of product-level nutritional positioning and helps inform personalization strategies for different consumer needs.

<img width="890" height="1389" alt="sugar distribution across fruits" src="https://github.com/user-attachments/assets/da9a2429-e29d-402c-8551-1877bbe2c5ae" />

### Data Sources
Nutritional data was obtained through the Fruityvice API. The API provided nutritional information for a wide variety of fruits. A CSV snapshot is also included for reproducibility if the API is unavailable. 

### Dataset characteristics
| Column Name      | Description |
|------------------|------------|
| `name`           | Name of the fruit |
| `id`             | Unique identifier assigned to the fruit in the API |
| `family`         | Botanical family the fruit belongs to |
| `order`          | Botanical order classification |
| `genus`          | Botanical genus classification |
| `calories`       | Energy content per 100g (in kcal) |
| `fat`            | Total fat content per 100g (in grams) |
| `sugar`          | Total sugar content per 100g (in grams) |
| `carbohydrates`  | Total carbohydrate content per 100g (in grams) |
| `protein`        | Protein content per 100g (in grams) |

### Tools
- Python – Programming language used for data acquisition, data cleaning and exploratory data analysis

- Visual Studio Code (VS Code) – Development environment

- Pandas – Data structuring, aggregation, and pivot table analysis

- Matplotlib & Seaborn – Visualization of patterns, trends, and comparative distributions

### Data Preparation

To ensure the data was suitable for analysis, the following tasks were performed:

1. API Data Retrieval & Initial Inspection – Retrieved fruit data from the Fruityvice API and reviewed the JSON structure.
2. Data Structuring - Converted nested JSON responses into a structured Pandas DataFrame.
3. Handling Missing Values - Checked for null or incomplete entries and addressed inconsistencies where necessary.
4. Outlier Detection - Reviewed extreme nutritional values to ensure data reliability.
5. Data Formatting - Standardized column names and ensured appropriate data types for numerical analysis.

Note: An outlier was observed in the nutrient distributions. A correlation matrix was not performed because nutrients are measured in different units (e.g., calories vs. grams), which could lead to misleading interpretations.

### Exploratory Data Analysis

EDA involved exploring the nutritional fruit data to answer key questions, such as:

1. Sugar Distribution -  Which fruits have the highest and lowest sugar content?
2. Calorie overview - What is the average calorie value of all fruits?
3. Carbohydrate comparison - Find the fruits with the highest and lowest carbohydrate content.
4. Protein ranking - Find the top 5 fruits with the highest protein content.
5. Category filtering - Find all fruits with the word berry
6. Fat analysis - Which fruits contain the least fat content?
7. Genus-level aggregation - Create a pivot table that shows the average sugar content of fruits grouped by their genus.

### Personalized Insights

While the initial EDA focused on understanding nutrient distributions and comparative patterns, a deeper analysis was conducted to explore how these nutritional attributes align with different consumer health needs. The analysis considered example consumer categories such as:

1. Weight loss Focus – Fruits with lower calorie values\
2. Diabetes-Conscious Consumers – Fruits with lower sugar content
3. Fitness-Oriented Consumers – Fruits with relatively higher protein content
4. Plant-Based / Vegetarian Diets – Nutrient-dense fruits supporting balanced intake

### Implementation

The full technical implementation is available in the Jupyter Notebook:
👉 `Fruityvice Analysis.ipynb`

How to run the project:
```Python
1. Setup the environment

# Clone the repository
git clone <the-repository-url>
cd Nutritional-Product-Insight-Analysis

# Create a virtual environment (recommended)
python -m venv env

# Activate the environment
# Windows:
  env\Scripts\activate
# Mac/Linux:
  source env/bin/activate

# Install required packages
pip install -r requirements.txt

2. Open and run notebook

# Launch VS Code of Jupyter lab and run all
# Run the cells to reproduce the analysis and visualizations.
```

### Results

1. Sugar extremes: Jackfruit has high sugar, while gooseberry is naturally low — useful for health-conscious product positioning.
2. High-protein fruits for fitness: Hazelnut, dragonfruit, guava, passion fruit, and avocado are relatively higher in protein, with hazelnut being particularly calorie-dense (important for portion guidance).
3. Low-fat options: Persimmon, pomelo, melon, cranberry, lime, and green apple stand out as low-fat fruits for general health-focused marketing.
4. Berries: Certain berries like blueberry, cranberry, and gooseberry offer low-sugar, nutrient-dense alternatives for targeted consumer segments.
5. Purpose-based segmentation: Analysis supports categorization of fruits for different consumer needs (weight management, diabetes-conscious, fitness-focused), providing a framework for product positioning and personalized marketing.

Note: More detailed tables, rankings, and visualizations are available here `Fruityvice Analysis.ipynb`

### Business Impact

The analysis strengthens strategic decision-making by transforming raw nutritional data into structured, comparable insights. Specifically, it contributes in the following ways:

Improved Nutritional Visibility – Provides a clearer overview of how fruits differ across key metrics such as sugar, calories, protein, and fat.

Category-Level Positioning Insight – Enables comparison across fruit groups (e.g., genus-level aggregation), supporting better product-level positioning decisions.

Health-Oriented Segmentation Support – Structures nutritional attributes in a way that aligns with different consumer lifestyle goals (e.g., weight management, fitness focus, sugar-conscious consumers).

Data-Informed Personalization Enablement – Makes it easier for marketing and product teams to tailor messaging and highlight relevant nutritional strengths for specific target audiences.

Reduced Decision Complexity – Summarizes complex nutritional patterns into visual and structured formats, supporting faster and more confident decision-making.

### Recommendations
Based on the analysis, fruit companies and product teams can consider the following:

1. Targeted Product Positioning – Use nutrient profiles to tailor fruits for different consumer needs, e.g., low-calorie fruits for weight-conscious consumers and protein-rich options for fitness-focused segments.
2. Balanced Product Combinations – For products containing higher-calorie, high-protein fruits like hazelnut, combine them with lower-calorie fruits such as dragonfruit, guava, or passion fruit to create balanced options.
3. Marketing Segmentation – Highlight specific nutritional attributes (low sugar, high protein, low fat) in marketing campaigns to appeal to distinct consumer groups.
4. Category-Level Insights – Use genus-level sugar or nutrient patterns to design product bundles or create specialized fruit mixes for targeted health or lifestyle goals.
5. Decision Support – Continue using structured data analysis to identify emerging patterns, optimize ingredient proportions, and guide future product development.

### Limitations
1. Limited Data Scope – The analysis relies entirely on the Fruityvice API, which may not include all fruits or the latest nutritional information. For instance, nutrients like vitamins and minerals were not included
2. No Direct Health Recommendations - While nsights are for decision support and product positioning only, they are not medical or dietary advice.

Future work could integrate multiple data sources, expand nutrient coverage, and incorporate consumer preference or regional availability data to enhance product insights.

### References
- Fruityvice API - Nutritional fruit data
- Python (Pandas, Matplotlib, Seaborn) – Data analysis and visualization tools
- [Hazelnut calories check](https://foods.fatsecret.com/calories-nutrition/usda/hazelnuts-or-filberts-nuts?portionid=59802&portionamount=100.000)

