# Nutritional-Product-Insight-Analysis

### Project Overview

This project analyzes fruit nutritional data to uncover patterns that support product development and marketing decisions. The analysis seeks to improve understanding of product-level nutritional positioning and helps inform personalization strategies for different consumer needs.

### Data sources
Nutritional data was obtained through the Fruityvice API. The API provided nutritional information for a wide variety of fruits. 

### Tools
- Python – Programming language used for data acquisition, data cleaning and exploratory data analysis

- Visual Studio Code (VS Code) – Development environment

- Pandas – Data structuring, aggregation, and pivot table analysis

- Matplotlib & Seaborn – Visualization of patterns, trends, and comparative distributions

### Data Cleaning/Preparation

To ensure the data was suitable for ana,ysis, the following tasks were performed:

1. API Data Retrieval & Initial Inspection – Retrieved fruit data from the Fruityvice API and reviewed the JSON structure.
2. Data Structuring - Converted nested JSON responses into a structured Pandas DataFrame.
3. Handling Missing Values - Checked for null or incomplete entries and addressed inconsistencies where necessary.
4. Outlier Detection - Reviewed extreme nutritional values to ensure data reliability.
5. Data Formatting - Standardized column names and ensured appropriate data types for numerical analysis.

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

1. Weight loss Focus – Fruits with lower calorie values

2. Diabetes-Conscious Consumers – Fruits with lower sugar content

3. Fitness-Oriented Consumers – Fruits with relatively higher protein content

4. Plant-Based / Vegetarian Diets – Nutrient-dense fruits supporting balanced intake




### Business Impact

The analysis strengthens strategic decision-making by transforming raw nutritional data into structured, comparable insights. Specifically, it contributes in the following ways:

Improved Nutritional Visibility – Provides a clearer overview of how fruits differ across key metrics such as sugar, calories, protein, and fat.

Category-Level Positioning Insight – Enables comparison across fruit groups (e.g., genus-level aggregation), supporting better product-level positioning decisions.

Health-Oriented Segmentation Support – Structures nutritional attributes in a way that aligns with different consumer lifestyle goals (e.g., weight management, fitness focus, sugar-conscious consumers).

Data-Informed Personalization Enablement – Makes it easier for marketing and product teams to tailor messaging and highlight relevant nutritional strengths for specific target audiences.

Reduced Decision Complexity – Summarizes complex nutritional patterns into visual and structured formats, supporting faster and more confident decision-making.
