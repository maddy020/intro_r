
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Welcome to the NHS-R Community Introduction to R and R Studio! <a alt="NHS-R Community's logo" href='https://nhsrcommunity.com/'><img src='https://nhs-r-community.github.io/assets/logo/nhsr-logo.svg' align="right" height="80" /></a>

<!-- badges: start -->
<!-- badges: end -->

## Attending the course?

If you are attending the course all the course materials and preparation
instructions are
[here](https://philosopher-analyst.netlify.app/intro-r/nhsr-intro/prework/).

## Are you wanting to update or use the slide code?

This repository is split into 3 areas:

-   [RMarkdown files and dependency
    files](https://github.com/nhs-r-community/intro_r/tree/main) -
    slides have been built in {xaringan} which requires the css, img and
    libs folder to render
-   [html
    pages](https://github.com/nhs-r-community/intro_r/tree/gh-pages) -
    are automatically rendered using GitHub actions (no need to knit
    every file!) and are kept on a separate branch. The html files are
    published though GitHub
    [here](https://nhs-r-community.github.io/intro_r/) and being
    {xaringan} they are interactive and accessible
-   [data files](https://github.com/nhs-r-community/intro_r_data/) are
    in a separate repository to help learners access the data files
    separate to the code for the slides

## Set-up

You will need to have R, R tools (on Windows), RStudio, and git
installed in order to use this project locally.

[Clone the
repository](https://happygitwithr.com/existing-github-first.html#new-rstudio-project-via-git-clone),
then run the following code chunk to initialise the project.

``` r
# the data directory is a git submodule, which needs to be downloaded
if (length(dir("data", ".csv")) == 0) {
  system("git submodule init")
  system("git submodule update")
}
# install all of the required packages
renv::restore()
# download fontawesome icons used in slides
icons::download_fontawesome()
```

Once you have run these steps, in RStudio you can open the individual
Rmarkdown documents and render each file. Alternatively, you can render
all of the slides at once using the “Build All” button on the “Build”
tab in RStudio.

## Spotted a mistake?

Please let us know if there are mistakes or improvements by creating an
[issue](https://github.com/nhs-r-community/intro_r/issues).
