## Overview

`PlasmodiumgenomeData` is a data package that provides genome sequences for various *Plasmodium* species. The data is designed to be hosted on **Bioconductor's ExperimentHub**, enabling users to access large genomic datasets on-demand. This package supports genomic and bioinformatics research focused on *Plasmodium* species, which are responsible for malaria.

## Features

- Genome data for multiple *Plasmodium* species, including:
  - *Plasmodium falciparum*
  - *Plasmodium vivax*
  - *Plasmodium malariae*
  - *Plasmodium knowlesi*
  - *Plasmodium ovale*
- Data is stored in `.rds` format and optimized for fast access via **ExperimentHub**.
- Includes metadata describing each dataset.

## Installation

Once accepted by Bioconductor, the package can be installed using:

```R
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

BiocManager::install("PlasmodiumgenomeData")
```

Before submission to Bioconductor, you can install the development version directly from GitHub:

```R
devtools::install_github("ocheab/PlasmodiumgenomeData")
```

## Usage

Access the genome data using the `ExperimentHub` package:

```R
library(ExperimentHub)

# Initialize ExperimentHub
hub <- ExperimentHub()

# Search for PlasmodiumgenomeData datasets
query(hub, "PlasmodiumgenomeData")

# Load a specific dataset (replace EH12345 with the actual ID)
genome_data <- hub[["EH12345"]]

# Explore the dataset
print(genome_data)
```

## Data Sources

The genome data was retrieved from **NCBI** and includes sequences for multiple *Plasmodium* species. For detailed metadata about each dataset, refer to the `metadata.csv` file in the package.

## Contributing

We welcome contributions to improve this package. If you encounter any issues or have suggestions, please create an issue in the GitHub repository.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Maintainer

George Oche Ambrose 
Email: [ocheab1@gmail.com](mailto:ocheab1@gmail.com)
