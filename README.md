# Higher Education Clustering Analysis

This project analyzes U.S. higher education institutions by grouping them into clusters based on cost, financial aid, and student success outcomes. Using K-Means clustering in Python and a Tableau dashboard for visualization, this analysis helps identify patterns in how colleges serve students across financial and academic dimensions.

## Project Overview

The purpose of this project is to explore whether institutions of higher education in the U.S. can be meaningfully grouped by their affordability and outcomes. The analysis uses clustering to categorize institutions and visualizations to make the results interpretable to non-technical audiences.

Key clustering features:
- Total Cost of Attendance
- Percent of students receiving Pell Grants
- Percent of students receiving Federal Loans
- Four-year graduation rate
- Three-year student loan default rate

These features represent both access and success — the financial burden students face and how likely they are to complete a degree or default on loans.

## Objectives

- Perform K-Means clustering to segment institutions by cost, aid, and outcomes
- Assign readable cluster labels to improve interpretability
- Clean and standardize ZIP codes for geographic mapping
- Visualize the data in Tableau to support filtering and exploration by cluster, state, or ZIP region

## Data Sources

- [U.S. Department of Education - College Scorecard](https://collegescorecard.ed.gov/data/)
- ZIP code to geographic coordinates reference data (latitude and longitude)

The data was cleaned and filtered to include only institutions with valid entries for the clustering features.

## Methodology

1. **Data Cleaning and Preparation**
   - Selected relevant financial aid and outcome variables
   - Removed rows with missing values
   - Extracted 5-digit ZIP codes from ZIP+4 entries
   - Merged ZIP codes with external latitude and longitude data

2. **Clustering with K-Means**
   - Standardized numeric features using `StandardScaler`
   - Applied K-Means clustering with `k=3`
   - Sorted clusters by graduation rate and assigned descriptive labels:
     - High-Risk, High-Aid Institutions
     - Middle-Tier, Mixed-Aid Institutions
     - Elite, Low-Aid Institutions

3. **Visualization in Tableau**
   - Created a map using accurate geographic coordinates
   - Built interactive views: parallel coordinates, scatter plots, and cluster distribution
   - Enabled dynamic filters for cluster, state, and cost range

## Tableau Dashboard

The final dashboard includes:
- A scatter plot showing graduation rate vs. total cost, colored by cluster
- A U.S. map of institutions with cluster overlays
- A bar chart showing the count of institutions per cluster
- Filters for state, ZIP prefix, and cluster label

View the interactive dashboard here:  
[Tableau Public Dashboard Link]([https://public.tableau.com/app/profile/YOUR-LINK-HERE](https://public.tableau.com/app/profile/adam.gilbert7036/viz/ClusteringU_S_CollegesbyCostAidGraduationOutcomes/ClusteringU_S_CollegesbyCostAidGraduationOutcomes))

## Repository Contents

- `Higher-Ed-Analysis.ipynb`: Jupyter notebook with all data cleaning, clustering, and CSV export logic
- `clustered_institutions_with_coords.csv`: Final dataset including institution names, cluster labels, and latitude/longitude
- `us_zip_data.csv`: ZIP code reference file with geographic coordinates
- `dashboard_screenshot.png`: Static image preview of the Tableau dashboard

## Skills Demonstrated

- Exploratory data analysis and preprocessing with pandas
- Clustering with scikit-learn
- String manipulation and ZIP code standardization
- Merging external geographic datasets
- Tableau dashboard development
- Geographic visualization and interactive filtering

## Next Steps

Possible extensions to the project include:
- Incorporating net price by income bracket
- Performing PCA to reduce dimensionality before clustering
- Adding metrics on student debt and earnings outcomes
- Comparing clusters across public vs. private institutions

## License

This project uses publicly available data from the U.S. Department of Education and ZIP code data for non-commercial purposes.
