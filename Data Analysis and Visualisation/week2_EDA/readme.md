### Week 2 – Data Preprocessing & Exploration
**Goal:** Learn to clean, transform, and explore datasets.

---

#### **1. Free PowerPoint Slides**
- **“Data Preprocessing in Data Mining”** – Covers handling missing values, outlier detection, normalization, and encoding.  
  

- **“Exploratory Data Analysis (EDA) in Python”** – Practical examples with pandas, matplotlib, seaborn.  
  

- **“Data Cleaning and Preprocessing”** – Brief slides on data quality, transformation, and integration.
  

#### **2. Dataset Suggestions (Free & Open)**
- **Titanic Dataset** (Kaggle, CSV format) – Ideal for missing value handling, encoding categorical features.  
  [https://www.kaggle.com/c/titanic/data](https://www.kaggle.com/c/titanic/data)  

- **Iris Dataset** (UCI Machine Learning Repository) – Good for normalization & basic EDA.  
  [https://archive.ics.uci.edu/ml/datasets/iris](https://archive.ics.uci.edu/ml/datasets/iris)  

- **Adult Income Dataset** (UCI) – Best for encoding categorical variables and scaling.  
  [https://archive.ics.uci.edu/ml/datasets/adult](https://archive.ics.uci.edu/ml/datasets/adult)



#### **3. Practical Activities**
1. **Loading Data**
   ```python
   import pandas as pd
   df = pd.read_csv('titanic.csv')
   df.head()
   ```

2. **Handling Missing Values**

   ```python
   # Drop missing rows
   df.dropna(inplace=True)

   # Or fill missing
   df['Age'].fillna(df['Age'].mean(), inplace=True)
   ```


3. **Encoding Categorical Variables**

   ```python
   df = pd.get_dummies(df, columns=['Sex', 'Embarked'])
   ```

4. **Normalizing Data**

   ```python
   from sklearn.preprocessing import MinMaxScaler
   scaler = MinMaxScaler()
   df[['Age', 'Fare']] = scaler.fit_transform(df[['Age', 'Fare']])
   ```

5. **Basic EDA**

   ```python
   import seaborn as sns
   sns.heatmap(df.corr(), annot=True, cmap='coolwarm')
   ```


#### **4. Submission**

* Push `.ipynb` notebook with:

  * Data cleaning steps
  * Encoded and normalized dataset
  * At least 3 visualizations
* Include a short summary of findings.
# Types of Datasets

Datasets can be categorized in several ways depending on their structure, source, and intended use.  
Below are the most common classifications:

---

## 1. **Structured Datasets**
- **Definition:** Data organized in a predefined format (rows and columns) such as databases and spreadsheets.
- **Examples:**  
  - Employee records in a company database  
  - Financial transaction logs  
- **Common Formats:** CSV, XLSX, SQL databases

---

## 2. **Unstructured Datasets**
- **Definition:** Data without a fixed structure, often text-heavy or media-based.
- **Examples:**  
  - Social media posts  
  - Images and videos  
  - Emails and chat logs  
- **Common Formats:** TXT, JSON, JPEG, MP4

---

## 3. **Semi-Structured Datasets**
- **Definition:** Data that does not reside in a strict table but has some organizational elements (tags, metadata).
- **Examples:**  
  - XML documents  
  - JSON data from APIs  
  - Sensor data with labeled attributes  
- **Common Formats:** XML, JSON

---

## 4. **Time-Series Datasets**
- **Definition:** Data collected over time in sequential order.
- **Examples:**  
  - Stock prices over time  
  - Weather measurements  
  - Website traffic logs  
- **Common Formats:** CSV, XLSX, specialized time-series databases

---

## 5. **Spatial (Geospatial) Datasets**
- **Definition:** Data representing locations, shapes, or geographic features.
- **Examples:**  
  - GPS coordinates  
  - Satellite imagery  
  - Maps with layers of information  
- **Common Formats:** SHP, GeoJSON, KML

---

## 6. **Open Datasets**
- **Definition:** Freely available datasets for public use without restrictions.
- **Examples:**  
  - Government census data  
  - Public health records (non-sensitive)  
  - OpenStreetMap data  
- **Common Formats:** CSV, JSON, API endpoints

---

## 7. **Proprietary Datasets**
- **Definition:** Datasets owned by organizations, often requiring purchase or a license to use.
- **Examples:**  
  - Commercial market research data  
  - Private customer databases

---

## Summary Table

| Dataset Type        | Structure        | Example Use Case                      |
|---------------------|------------------|----------------------------------------|
| Structured          | Tabular          | Sales reports, HR databases           |
| Unstructured        | Freeform         | Social media content, videos          |
| Semi-Structured     | Tagged/Metadata  | Web scraping JSON, XML feeds          |
| Time-Series         | Sequential       | Stock market analysis, IoT sensors    |
| Spatial             | Geographic       | Mapping, GPS navigation               |
| Open                | Public access    | Research projects, civic tech apps    |
| Proprietary         | Restricted       | Business intelligence, paid analytics |


---

