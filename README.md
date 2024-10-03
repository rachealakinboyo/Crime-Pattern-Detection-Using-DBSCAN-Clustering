
# Crime Analysis Using DBSCAN Clustering

This project involves analyzing crime data from various boroughs in London, UK, using DBSCAN clustering to identify crime hotspots. The dataset used is sourced from the UK Police Data Portal.

## Table of Contents
- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Results](#results)
- [License](#license)

## Project Overview

In this project, we explore crime data to identify spatial patterns and hotspots of crime using machine learning models. DBSCAN clustering is used to group similar crime locations based on their latitude and longitude. The analysis also includes exploratory data analysis (EDA) to visualize crime types, outcomes, and crime locations.

## Data Source

The data is sourced from the [UK Police Data Portal](https://data.police.uk/), which provides street-level crime, outcome, and location data for England, Wales, and Northern Ireland. The dataset used spans from 2021 to 2024 and contains 45,822 rows and 13 columns.

**Key features in the dataset**:
- Crime type (e.g., burglary, theft, violent crime)
- Date of occurrence (year, month, day)
- Location (latitude and longitude)
- Outcome of investigation (e.g., suspect charged, case dropped)

## Installation

To run this project, you need to install the following dependencies:

\`\`\`bash
pip install -r requirements.txt
\`\`\`

The dependencies include:
- \`pandas==1.5.3\`
- \`numpy==1.24.0\`
- \`matplotlib==3.6.3\`
- \`seaborn==0.12.1\`
- \`scikit-learn==1.1.3\`
- \`joblib==1.2.0\`

## Usage

1. **Clone the repository**:
   \`\`\`bash
   git clone https://github.com/your-username/crime-analysis-ML-project.git
   cd crime-analysis-ML-project
   \`\`\`

2. **Load the dataset**: Place your dataset (\`merged_data.csv\`) in the appropriate directory or update the path in the script.

3. **Run the project**:
   - You can run the Jupyter notebook to see the analysis:
     \`\`\`bash
     jupyter notebook crime_analysis.ipynb
     \`\`\`

4. **Model training**: The DBSCAN clustering model is trained and saved as a \`pkl\` file using the \`joblib\` library.

## Project Structure

\`\`\`
.
├── crime_analysis.ipynb       # Jupyter notebook containing the full analysis
├── merged_data.csv            # The dataset (not included, must be downloaded)
├── london_crime_detection_dbscan_model.pkl  # Saved model
├── requirements.txt           # Required Python packages
└── README.md                  # Project documentation
\`\`\`

## Results

### Silhouette Scores:
- **Silhouette Score for DBSCAN on Training Set**: \`0.9536\`
- **Silhouette Score for DBSCAN on Test Set**: \`0.9002\`

The high silhouette scores indicate that the DBSCAN model is effective at clustering the data, with minimal noise and well-separated clusters.

### Exploratory Data Analysis:
1. **Crime Type Distribution**: Theft-related offenses and violent crimes are the most prevalent in the dataset.
2. **Outcome Distribution**: A large number of cases either remain unsolved or fail to lead to prosecution.
3. **Crime Count by LSOA (Lower Super Output Area)**: The **City of London 001F** has the highest crime count, followed by **City of London 001G** and **City of London 001E**.
4. **Geospatial Distribution of Crimes**: Crime incidents are concentrated in specific regions, especially around latitude 51.52 and longitude -0.10.

### Model Analysis:
The DBSCAN clustering identifies consistent crime hotspots across both the training and test datasets. The model performs well, achieving high silhouette scores for both the training (\`0.9536\`) and test datasets (\`0.9002\`), indicating that the clusters are well-defined and consistent.

## License

This project is **proprietary** and may not be modified or distributed without explicit permission from the author. For inquiries about using or modifying the contents of this repository, please contact [your-email@example.com].
