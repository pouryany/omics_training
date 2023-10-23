## Introductory ’omics training

Welcome to the introductory ’omics training short course.

The purpose of this training is to provide a beginners’ bioinformatics
toolbox to analyze ’omics data.

This page will update periodically. Please contact
`pnaderiy [at] bidmc [dot] harvard [dot] edu` for any questions or
suggestions you may have about the codes.

## Tentative topics

### System setup

1.  **Setting Up R and RStudio**
    -   Installation of R, a popular programming language for
        statistical analysis.
    -   Installation of RStudio, a user-friendly integrated development
        environment (IDE) for R.
    -   Basic orientation to the RStudio interface and its features.
2.  **Introduction to R Scripting**
    -   Basic operations in R.
    -   Basic data analysis with R
    -   Tidyverse and dplyr.
    -   Visualization.
3.  **Setting Up Python and Jupyter Notebook**
    -   Installation of Python, a versatile programming language widely
        used in bioinformatics.
    -   Installation of Anaconda, a distribution of Python that includes
        essential data science libraries and package management tools.
    -   Creating and managing Python environments using Conda to isolate
        dependencies.
    -   Introduction to Jupyter Notebook, an interactive web-based
        environment for data analysis.
4.  **Introduction to Bash Scripting**
    -   Overview of the Bash shell and its importance in bioinformatics.
    -   Basic commands and navigation within the command-line interface.
    -   Understanding file systems, directories, and paths in a
        Unix-like environment.
5.  **Introduction to GitHub and Version Control**
    -   Understanding the importance of version control in collaborative
        coding and data analysis.
    -   Introduction to Git, a distributed version control system.
    -   Overview of GitHub, a popular platform for hosting Git
        repositories and collaborating with others.

### Basic genomics

1.  **Introduction to Sequencing Technologies**
    -   Overview of RNA-Seq and DNA-Seq technology.
    -   The process of library preparation, sequencing, and data
        acquisition.
    -   Applications in quantifying gene expression and alternative
        splicing.
2.  **Introduction to RNA-Seq for gene expression analysis**
    -   Reading and inspecting RNA-Seq data.
    -   Preliminary QC: outlier detection and normalization.
    -   Basic differetial expression analysis.
    -   Understanding batch effects.
3.  **Functional Annotation and Analysis**
    -   Introduction to gene ontology (GO), pathways, and functional
        annotation terms.
    -   How functional annotation helps in understanding the roles of
        genes.
    -   Resources for accessing functional annotation data.
    -   How pathway analysis tools help in understanding complex
        biological processes.
    -   Examples of pathway analysis in disease research.
4.  **Genomics Databases**
    -   Introduction to databases like Gene Expression Omnibus (GEO) and
        The Cancer Genome Atlas (TCGA).
    -   How to access and retrieve genomics data from these resources.
    -   Real-world examples of studies using publicly available
        datasets.
5.  **Analyzing Whole Genome and/or Exome Sequencing**
    -   Overview of how WGS/WES reveals heterogeneity within cell
        populations.
    -   Applications in developmental biology, immunology, and cancer
        research.
6.  **RNA-Seq Module 2**
    -   Small RNA-Seq.
    -   Alternative Splicing.
    -   Modeling complex statistical designs.
    -   Batch effect correction methods.
    -   Unsupervised clustering algorithms.
7.  **Functional Analysis Module 2**
    -   Advanced pathway analysis.
    -   Analysis for gene interaction networks.
8.  **Sequencing DNA Methylation and Chromatic accessibility**
    -   ATAC-Seq
    -   DNA-Methylation arrays and Bisulfite Sequencing.
    -   Functional analysis of ATAC-Seq and Methylation data.
9.  **Single-Cell Genomics**
    -   Overview of single-cell RNA sequencing (scRNA-Seq) and its
        importance.
    -   How scRNA-Seq reveals heterogeneity within cell populations.
    -   Applications in developmental biology, immunology, and cancer
        research.
10. **Integration of Multi-Omics Data**
    -   Explanation of multi-omics approaches (genomics,
        transcriptomics, proteomics, metabolomics).
    -   How integrating different types of omics data provides a
        holistic view of biology.
    -   Challenges and methods for data integration.
11. **Case Studies**
    -   Present real-world examples of genomics studies.
12. **Hands-On Activities**
    -   Provide participants with practical exercises related to gene
        expression analysis or pathway analysis using publicly available
        datasets and bioinformatics tools.
13. **Future Directions**
    -   Discuss emerging trends in functional genomics research, such as
        single-cell multi-omics and spatial transcriptomics.
    -   Consider the potential impact of functional genomics on
        personalized medicine.

## Setting Up R and RStudio

### Basic installation

Here are the steps to install both R and RStudio:

1.  **Download R:** Visit the CRAN (Comprehensive R Archive Network)
    website: <https://cran.r-project.org/>. Choose and install the
    appropriate version of R for your operating system (Windows, macOS,
    or Linux).

2.  **Download RStudio:** Go to the RStudio download page:
    <https://www.rstudio.com/products/rstudio/download/>. Select the
    RStudio Desktop version that is compatible with your operating
    system.

### Useful tips

1.  **Check R Installation:** In RStudio, you can verify that R is
    correctly installed by opening the R console in the bottom-left
    panel and typing `R.version` and pressing Enter.

2.  **Install Packages:** There are three main sources of installing R
    packages

    -   **CRAN Packages:** There are common R libraries. You can install
        R packages (libraries) using the `install.packages()` function.
        For example, to install the `ggplot2` package, you would run
        `install.packages("ggplot2")` in the R console.

    -   **Bioconductor Packages:** Bioconductor is a major project to
        standardize the development, support, and release of
        Bioinformatics software packages. After installing Bioconductor
        manager package in R (using `install.packages("BiocManager")`),
        you can install specific Bioconductor packages using
        `BiocManager::install("package name")` command. Read more on
        Bioconductor packages here:
        <https://www.bioconductor.org/install/>. Example Bioconductor
        package installation bellow.

              ```r
              if (!require("BiocManager", quietly = TRUE))
                  install.packages("BiocManager")
              BiocManager::install("PanomiR")
              ```

    -   **Github Packages:** Some packages are only available through
        GitHub, mainly because they are still in development. This
        packages can be installed using `devtools`. First, install the
        `devtools` library. Next, provide a GitHub address to install a
        specific package. See example below.

              ```r
              devtools::install_github("pouryany/PanomiR")
              ```

        ### Additional advanced tips

3.  **Having multiple versions of R:** Sometimes you may need to work
    with multiple versions of R. Use RSwitch to manage multiple versions
    of R <https://rud.is/rswitch/>.

4.  **More on installing R and R packages:** Use the following book to
    read and learn more about installing R and related packages
    <https://rstudio-education.github.io/hopr/starting.html#how-to-download-and-install-r>.

That’s it! You should now have R and RStudio set up on your computer,
ready for data analysis and scripting in the R programming language.
