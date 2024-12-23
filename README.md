# Web Scraping, Data Transformation, and ETL Pipeline with AWS Glue

## Project Overview

This project was designed to practice and learn the **ETL (Extract, Transform, Load)** pipeline using **AWS Glue** and **Amazon S3** while analyzing perfume product data from **Ulta's website**. The goals were twofold:

1. **ETL Pipeline Practice**: Gain hands-on experience with the ETL process using **AWS Glue** and **S3**.
2. **Perfume Popularity Analysis**: Understand which perfumes are more popular and better-rated on Ulta’s website by analyzing product ratings and reviews.

---

## Project Breakdown

### 1. Web Scraping (Using Selenium and BeautifulSoup)

- **Objective**: Scrape perfume product data (name, brand, reviews) from **Ulta's website**.
- **Technologies**: `Selenium`, `BeautifulSoup`, `pandas`
- **Output**: A CSV file containing the scraped data was saved and uploaded to **Amazon S3** for further transformation.

**Files:**
- `ScrapingUltaPerfume.ipynb`: Web scraping script to collect data from Ulta.
- `ulta_perfume_data.csv`: Raw data containing product names, brands, and reviews.

---

### 2. Data Transformation and Loading (Using AWS Glue)

- **Objective**: Use **AWS Glue** to transform the scraped data:
  - Add a **Total Weighted Average Rating** column considering both star ratings and the number of reviews.
  - Group data by **brand** to analyze the popularity and average ratings of perfumes.
  - Load the transformed data back into **Amazon S3** for further analysis.

The transformation and loading process involved:
- **Extract**: Loaded the scraped data from **S3** into AWS Glue.
- **Transform**: 
  - Calculated a **weighted average rating** using both the star rating and the number of reviews.
  - Grouped the data by **brand** to analyze average ratings for each perfume brand.
- **Load**: The transformed data was saved into a new CSV file and uploaded back into **Amazon S3** for storage and further analysis.

**Files:**
- `TransformingLoadingData.ipynb`: Jupyter Notebook for transforming and loading the data using AWS Glue.

---

## Technologies Used

- **Selenium**: For web scraping and automating data extraction from Ulta.
- **BeautifulSoup**: For parsing HTML and extracting product data.
- **pandas**: For managing and saving data.
- **AWS Glue**: For transforming and processing data in the ETL pipeline.
- **Amazon S3**: For storing both raw and transformed data.

---

## How to Use

1. **Run Web Scraping**:
   - Execute `ScrapingUltaPerfume.ipynb` to scrape data from Ulta.
   - Data will be saved as `ulta_perfume_data.csv` and uploaded to **S3**.

2. **Transform and Load Data Using AWS Glue**:
   - Use the **AWS Glue Console** to run `TransformingLoadingData.ipynb` for both transforming and loading the data.
   - Adds a **Total Weighted Average Rating** column, groups data by **brand**, and loads the transformed data back into **Amazon S3**.

---

## Files in This Repository

- `ScrapingUltaPerfume.ipynb`: Code for scraping product data from Ulta.
- `ulta_perfume_data.csv`: The original CSV file with scraped product data.
- `TransformingLoadingData.ipynb`: Jupyter Notebook for transforming and loading the data using AWS Glue.

---

This project provides a full pipeline for scraping, transforming, and analyzing data using AWS services, with a focus on understanding perfume product ratings and popularity on Ulta's website.
