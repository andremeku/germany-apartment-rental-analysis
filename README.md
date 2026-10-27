# Apartment Rental Offers in Germany | Data Analysis

**Python • Pandas • Data Cleaning • Exploratory Data Analysis • Matplotlib • Seaborn**

A team data-analysis project exploring German apartment rental listings. The analysis examines rental prices, geographic differences, property characteristics, and data quality to better understand apartment offerings and support tenant-facing recommendations.

> **Project context:** Group G — Team 3. This was a collaborative project; my role was **Data Analyst**. The accompanying notebook is a portfolio-friendly refactoring of the team's original analysis, not a claim of sole authorship.

## Project overview

The source notebook loads a dataset of **268,850 apartment listings and 49 columns** from an ImmoScout24-based rental offers dataset. The accompanying team presentation summarizes a separate analysis view as approximately **175.3k offers (2018–2020)**; these two figures should not be assumed to represent the same processing stage.

**Research questions**
- How do rental prices differ across German regions?
- Which property characteristics can help describe apartment offerings?
- What data-cleaning steps are necessary before drawing conclusions?
- How can descriptive statistics and visualizations support rental-market decisions?

## My contributions and tools

The group presentation lists my role as **Data Analyst**. The shared project materials document a workflow covering data preparation, analysis, and visualization. The original code uses Python, Pandas, NumPy, Matplotlib, and Seaborn; the group presentation also references **Excel** and **Tableau**.

## Analysis workflow

1. **Import data:** Load apartment listings from a CSV file.
2. **Inspect data quality:** Review types, missing values, and candidate identifier duplicates.
3. **Clean data:** Convert relevant columns to appropriate types, remove records without rental prices, and remove columns with more than 30% missingness (matching the original notebook's approach).
4. **Normalize categories:** Group infrequent `regio2` values under `Other` and fill missing `condition` values with `Other`.
5. **Explore rental patterns:** Visualize rent distribution, differences across regions, and rent by budget band; inspect numeric correlations and year-of-construction distributions.

The notebook uses a reproducible random sample of up to 10,000 cleaned listings for visualizations. **This version has not been executed against the full source data in this package**, because the original large dataset is not redistributed here.

## Repository structure

```text
.
├── README.md
├── notebooks/
│   └── apartment_rental_analysis.ipynb
├── data/
│   └── README.md
├── requirements.txt
└── .gitignore
```

## How to run

1. Download or clone the repository.
2. Install Python 3.10+ and the requirements:

   ```bash
   pip install -r requirements.txt
   ```

3. Obtain the original dataset using the source link given in the notebook (subject to its sharing permissions), and save it as **`data/data_apartment.csv`**. The notebook also includes an optional download cell using `gdown`.
4. Open **`notebooks/apartment_rental_analysis.ipynb`** in Jupyter Notebook or Google Colab.
5. Run the cells from top to bottom. If working in Colab, upload the CSV to the expected `data/` folder or let the optional download cell retrieve it if accessible.

**Data note:** The original notebook's source data was approximately 285 MB, so it is intentionally excluded from the repository. Please verify the dataset's terms and availability before redistributing it.

## Source material and attribution

- **Dataset:** ImmoScout24-based apartment rental offers data, accessed through the Google Drive link documented in the original group notebook. This repository does not claim to own or license the underlying listings data.
- **Project:** *Apartment Rental Offers in Germany Analysis*, Group G — Team 3.
- **Team collaboration:** Group presentation credits four members (Dylan, Eko, Andre, Eric) with distinct responsibilities. Credit and individual contributions should be preserved when describing this work.

## Notes on this portfolio edition

The submitted notebook contained a few reproducibility issues (Colab-only file paths, `inplace=True` assignment, and duplicate-check errors). This edition reorganizes the analysis and corrects those issues. **The original analysis and presentation are not reproduced verbatim or claimed to have been independently validated.**
