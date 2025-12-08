
# Zimbabwe Business Directory Processing Pipeline

## Overview
This project provides a comprehensive workflow for creating a clean, deduplicated, and geographically enriched business directory for Zimbabwe. The pipeline processes raw business listings from various online directories, performs data cleaning and deduplication, and enhances the data with geographic and urbanization information.

## Project Structure
```
.
├── Data Source Identification.ipynb       # Identifies and collects business directories
├── Extracting companies from the directories.ipynb  # Web crawler for company data
├── Cleaning directories.ipynb            # Data cleaning and preprocessing
├── Deduplication second wave.ipynb       # Advanced deduplication of company records
├── Fuzzy Matching.ipynb                  # Fuzzy matching for duplicate detection
├── Geocoding Company Addresses.ipynb     # Converts addresses to coordinates
├── Degree of Urbanization.ipynb          # Classifies companies by urbanization level
├── Analysis and tabulations.ipynb        # Final analysis and reporting
└── README.md                             # This file
```

## Workflow

### 1. Data Collection
- **Data Source Identification**: Identifies and compiles a list of Zimbabwean business directories through web searches.
- **Web Crawling**: Extracts company listings from identified directories using a BFS-based crawler with checkpointing.

### 2. Data Cleaning
- Standardizes company names, addresses, and contact information.
- Removes or corrects malformed entries.
- Handles missing values and formats data consistently.

### 3. Deduplication
- **Fuzzy Matching**: Uses string similarity metrics to identify potential duplicates.
- **Record Linkage**: Implements advanced techniques to merge duplicate records while preserving unique information.

### 4. Geocoding
- Converts physical addresses to geographic coordinates (latitude/longitude).
- Uses Google Maps API or similar services for accurate geolocation.
- Handles partial or ambiguous addresses.

### 5. Urbanization Classification
- Classifies each business location by urbanization level using satellite imagery.
- Implements a multi-level classification system (Urban, Peri-urban, Rural).

### 6. Analysis & Visualization
- Generates statistical summaries of the business directory.
- Creates visualizations of business distribution and density.
- Produces reports on urbanization patterns and business clustering.

## Technical Requirements
- Python 3.8+
- Jupyter Notebook
- Key Python packages:
  - pandas, numpy
  - beautifulsoup4, requests
  - rapidfuzz
  - googlemaps (for geocoding)
  - earthengine-api (for urbanization analysis)
  - matplotlib, seaborn (for visualization)

## Setup Instructions
1. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

2. Set up API keys:
   - Google Maps API key (for geocoding)
   - Google Earth Engine credentials (for urbanization analysis)

3. Run notebooks in sequence as per the workflow.

## Usage
1. Start with `Data Source Identification.ipynb` to identify target directories.
2. Run `Extracting companies from the directories.ipynb` to crawl company data.
3. Proceed through the remaining notebooks in the order of the workflow.

## Output
- Cleaned and deduplicated business directory in CSV format.
- Geocoded company locations.
- Urbanization classification for each business.
- Analysis reports and visualizations.

## Contributing
Contributions are welcome! Please ensure to follow the existing code style and add tests for new features.

## License
[Specify License]

## Contact
watambwaperkins@gmail.com
```

This README provides a clear, structured overview of your project, making it easy for users and collaborators to understand and work with your codebase. The workflow is presented in a logical sequence, and each notebook's purpose is clearly explained.# From-Digital-Traces-to-Sampling-Frames