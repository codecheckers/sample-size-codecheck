---
editor_options: 
  markdown: 
    wrap: 72
---

## Sample size estimation for task-related functional MRI studies using Bayesian updating

### Code Checking materials

This repository contains the code and instructions for reproducing the
following paper:

Klapwijk, E. T., Jongerling, J., Hoijtink, H., & Crone, E. (2024, July
9). Sample size estimation for task-related functional MRI studies using
Bayesian updating. <https://doi.org/10.31234/osf.io/cz32t>

#### Contents

##### Main files

The following two [Quarto](https://quarto.org/) Markdown files (`*.qmd`)
are the main files containing the code to reproduce the figures and
tables:

-   `figures-cohens_d.qmd` (Figure 1 and 2; Table 2)

-   `figures-correlation.qmd` (Figure 3 and 4; Table 2)

##### HTML output

These files are rendered as hmtl pages containing all the individual and
collected figures:

-   `figures-cohens_d.html`

-   `figures-correlation.html`

##### PNG output

The individual .png files are saved in the following directories:

-   `figures-cohens_d_files/`

-   `figures-correlation_files/`

#### Workflow

The analysis for this paper is implemented in the statistical
programming language R. To reproduce the results, you will need
installed on your computer the [R
software](https://cloud.r-project.org/) itself, optionally (but
recommended) [RStudio
Desktop](https://posit.co/download/rstudio-desktop/), and
[Quarto](https://quarto.org/docs/get-started/).

-   You can download the compendium as a zip from from this URL:
    main.zip [insert repo url].

-   Or you can clone the repository: `git clone git@github.com:url`

Then:

-   open the `sample-size-codecheck.Rproj` file in RStudio

-   make sure you have the following packages installed:

    -   [`neuroUp`](https://eduardklap.github.io/neuroUp/), you can run
        `install.packages("neuroUp")` to install it

        -   this is the main package that was specifically developed for
            this paper.

        -   It also contains the 4 datasets used in the paper: You can
            run `?feedback` , `?gambling` , `?self_eval` , and
            `?vicar_char` for more information about the data source

    -   [`patchwork`](https://patchwork.data-imaginist.com/), you can
        run `install.packages("patchwork")` to install it

        -   this package is used to combine the different plots into the
            figures as presented in the manuscript

-   Finally, open `figures-cohens_d.qmd` and click **Render** to produce
    the html file and the individual png files
    (`figures-cohens_d_files/`), or run
    `quarto render figures-cohens_d.qmd` in the RStudio Terminal.

    -   **Runtime note**: due to the number of permutations (1000) used
        in the paper, it might take some time to run the whole document
        (e.g., it took \## minutes on a 4 core 32GB CPU virtual machine
        to render `figures-cohens_d.qmd`)

-   Do the same for the correlational analysis: open
    `figures-correlations.qmd` and click **Render** to produce the html
    file and the individual png files (`figures-correlations_files/`),
    or run `quarto render figures-correlations.qmd` in the RStudio
    Terminal.

-   If you do not have Quarto (or RStudio) installed, another (much less
    convenient) way to reproduce the analyses would be to run the
    individual code blocks as displayed in the .qmd (and .html) files
    subsequently in R.
