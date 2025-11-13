# *Staphylococcus aureus* colonization and bloodstream infection in very preterm infants

This repository contains all code and data used for the analysis reported in the publication:

“*Staphylococcus aureus* colonization and bloodstream infection in very preterm infants”
by Rebecca L. Knoll, MD, Daniel Podlesny, PhD, Ingmar Fortmann, MD, Wolfgang Göpel, MD, Michael Zemlin, Susan Lynch, PhD, Peer Bork, PhD, Stephan Gehring, MD, Christoph Härtel, MD.

## Repository Content:

  - Scripts/ .Rmd files ordered according to the analysis presented in the manuscript. Includes all code for statistical tests and figure generation to fully reproduce the findings.
  - Data/ Annotated data necessary to reproduce all statistical analyses.
  - renv.lock Captures the exact package versions used in the project.
  - renv/settings.json	Stores renv environment settings.
  - .Rproj Facilitates structured project organization in RStudio.

## Raw Data Availability:
    Raw sequencing data will be made available upon request.

## Reproducibility Guide:

Hardware used: System Information
    Device: MacBook Pro (2021)
    Processor: Apple M1 Max
    RAM: 64GB
    Operating System: macOS Sonoma v14.6.1

All statistical analyses were performed in the R environment (v4.5.1).

### Preparing the Data

Files numbered `00-*` and `01-*` are required to generate phyloseq objects from raw sequencing data and clinical metadata. To replicate the analysis without regenerating these objects, download the Data files and update the file paths accordingly in the scripts.

### Running the Analysis

Each `.Rmd` script begins by loading the necessary phyloseq objects. Ensure all required R packages are installed and loaded before execution.

#### Setting Up the Environment
To ensure full reproducibility, this repository includes an `renv.lock` file. Follow these steps to restore the exact package versions used in the analysis:

1. Clone this git repo into the working directory using the terminal
   ```bash
    git clone https://github.com/RebeccaLuise/s_aureus.git YOUR_DIRECTORY_HERE
    ```

2. Install `renv` if not already installed:
   ```r
   install.packages("renv")
   ```
3. Restore the project environment:
   ```r
   renv::restore()
   ```
   Installation & Execution Time Estimates

   On the specified hardware, approximate times for setting up and running the analysis are:

       Package Installation (renv::restore()): ~ 10 secondes
       Running All Scripts (rmarkdown::render()): ~ 30 minutes

### Running the Scripts
Once dependencies are installed, the `.Rmd` files can be run sequentially to reproduce the full analysis, including all statistical tests and visualizations. Open the `.Rproj` file in RStudio for an organized workflow.

### Zenodo DOI for publication:
DOI 10.5281/zenodo.17603738