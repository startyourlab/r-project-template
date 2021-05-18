<!--
**** README for the R Project Template repository
**** Origin URL: https://github.com/startyourlab/r-project-template
****
**** This README is your guide to setting up an R project for you and your team.
**** When you have completed setup, you should adapt the content of this README
**** to reflect your own project's specifications.
-->

[![Start Your Lab][syl-project-shield]][syl-project-url]

# R Project Template

This is a template repository for **using R with a team**. Use this template to leverage a shared set of configurations optimized for teams developing projects in R.

## Template Features

The R project you create with this template will be equipped with several helpful features:

- An RStudio project [`template.Rproj`](./template.Rproj) with smart defaults
- Package dependency management using [`renv`](https://github.com/rstudio/renv/)
- Environment-specific configuration using [`config`](https://github.com/rstudio/config)
- A comprehensive [`.gitignore`](./.gitignore) file to keep version tracking history clean
- An RMarkdown notebook [`notebook-template.Rmd`](./notebook-template.Rmd) with quick code chunk examples
- Generated document settings in [`_output.yaml`](./_output.yaml) for rendering RMarkdown notebooks with [`knitr`](https://yihui.org/knitr/)
- A dedicated [`R`](./R) folder for pure R scripts and reusable functions
- [GitHub Issues templates](./.github/ISSUE_TEMPLATE) for [filing bug reports, documentation updates, and feature requests](https://github.com/startyourlab/r-project-template/issues/new/choose)

## Prerequisites

### Local Applications

Please make sure that you have recent versions of R and RStudio installed.

This template is compatible with Git and GitHub _by default_. We suggest using **GitHub Desktop** to develop your project from this template. Please follow [these installation instructions](https://www.startyourlab.com/docs/github-desktop) if you have not already installed and configured your local GitHub Desktop application.

If you would like to use the [GitHub CLI](https://cli.github.com/), or the standard command line tools that come with your computer's Git installation, that's perfectly fine! However, this README will not discuss those methods of interaction in detail.

### R Packages

To take advantage of the optimized configuration settings included with this template, you must have the [`renv` package](https://rstudio.github.io/renv/articles/renv.html) installed on your local computer. While in an active RStudio session, simply run the following line of code in the Console.

```r
install.packages('renv')
```

## Installation

To use this template, click the green **Use this template** button or you can [click here](https://github.com/startyourlab/r-project-template/generate) to generate your project. It will ask you to 

1. Choose the repository's username/organization name, i.e., `yourlab`.
2. Name the repository, i.e., `our-new-r-project`.
3. Add a description of your project (optional, but highly recommended).

Once the repository is generated, you will be redirected to your new repository on GitHub.

### Clone the repository to your local machine

Go to the green **Code** button with a dropdown menu. There are two preferred methods, and we recommend using whichever you prefer:

#### 1. Open with GitHub Desktop

Click **Open with GitHub Desktop**, and pick a location in your personal file system to store it using the GitHub Desktop cloning interface. If using Linux, see option 2.

#### 2. Command line using HTTPS method

If using Linux or prefer the command line, you will use the HTTPS-based URL from the **Code** dropdown menu. The URL will look like `https://github.com/startyourlab/r-project-template.git`. Click the clipboard icon to copy it. From within your projects directory in the terminal, run `git clone ...`, replacing the "..." with the URL you just copied.

## Usage

### Renaming template files and content

Once the project is cloned to your computer, you need to rename the following files with your own names:

- `template.Rproj`, changing `template` to your repository name
- `notebook-template.Rmd`, changing `notebook-template` to the notebook
  name that you would like for the project's first notebook.
- `LICENSE.md`, replacing `Start Your Lab` with your name or lab's name.

### Local package installation

After renaming the above files, run the following line of code in your RStudio's Console:

```r
renv::restore()
```

This will install all of the foundational packages needed to begin developing your R project with this template. If installation encounters an error, restart your R session and try again. If it still does not work, please [reach out to the Start Your Lab team](https://www.startyourlab.com/community/support) with your issue and we can help you and your lab resolve it.

If you would like to install packages specific to your project's goals, now is the time to start! You can install packages like [`tidyverse`](https://www.tidyverse.org/), [`slackr`](https://mrkaye97.github.io/slackr/), or other packages on CRAN. For example, running

```r
install.packages('tidyverse')
```

will install `tidyverse` for your project. If you want to make this a package that the entire team uses for this project, run

```r
renv::snapshot()
```

to record the package with its version number in the `renv.lock` file, which keeps track of all the great packages you and your team use together.

## Commit your changes

Once files are renamed and packages are installed, it's time to commit these changes to GitHub. Using the GitHub Desktop application, review the files you changed. Make sure that you renamed and updated the appropriate [files above](#usage). Then, add a summary commit message, such as "update file names and configure project", and **Commit to `main`**. Finally, click **Push origin**, which will push your committed changes to the project's centralized copy of repository on GitHub. Your collaborators will now be able to pull these changes from GitHub into their local version of this repository.

## Get to work!

Now that everything is squared away, it's time to start work on your project. Open the renamed `.Rproj` file in RStudio, and start your project's development!

## Support

For questions about this template, please contact [Start Your Lab](https://www.startyourlab.com/community/support). You can also reach us on Twitter and Stack Overflow using the following buttons:

[![Twitter][twitter-shield]][twitter-url]
[![Stack Overflow][stackoverflow-shield]][stackoverflow-url]


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[syl-project-shield]: https://img.shields.io/badge/Start%20Your%20Lab-R%20Project%20Template-F4F4F4?logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4KPHN2ZyB3aWR0aD0iNzJweCIgaGVpZ2h0PSI3MnB4IiB2aWV3Qm94PSIwIDAgNzIgNzIiIHZlcnNpb249IjEuMSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxuczp4bGluaz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94bGluayI+CiAgICA8dGl0bGU+YnJhbmRtYXJrPC90aXRsZT4KICAgIDxnIGlkPSJQYWdlLTEiIHN0cm9rZT0ibm9uZSIgc3Ryb2tlLXdpZHRoPSIxIiBmaWxsPSJub25lIiBmaWxsLXJ1bGU9ImV2ZW5vZGQiPgogICAgICAgIDxnIGlkPSJpY29ucyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoLTI0NC4wMDAwMDAsIC0zODEuMDAwMDAwKSIgc3Ryb2tlPSIjMUUxRTI0IiBzdHJva2Utd2lkdGg9IjEuMzEzNDY5MTQiPgogICAgICAgICAgICA8ZyBpZD0iYnJhbmRtYXJrIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgyNDQuMDAwMDAwLCAzODEuMDAwMDAwKSI+CiAgICAgICAgICAgICAgICA8ZWxsaXBzZSBpZD0iT3ZhbCIgZmlsbD0iI0Y2RjdGOCIgY3g9IjM1Ljg4Njg3NjQiIGN5PSIzNS45MjI3NjMzIiByeD0iMzUuMjMwMTQxOCIgcnk9IjM1LjI2NjAyODciPjwvZWxsaXBzZT4KICAgICAgICAgICAgICAgIDxnIGlkPSJHcm91cCIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMzUuODk4OTQwLCAzNi4yNjg2NDUpIHJvdGF0ZSgtMzE1LjAwMDAwMCkgdHJhbnNsYXRlKC0zNS44OTg5NDAsIC0zNi4yNjg2NDUpIHRyYW5zbGF0ZSgxOC44OTg5NDAsIDE5LjI2ODY0NSkiPgogICAgICAgICAgICAgICAgICAgIDxyZWN0IGlkPSJSZWN0YW5nbGUiIGZpbGw9IiM0QzgyQTkiIHg9IjAiIHk9IjAiIHdpZHRoPSIxNC4zNTQ3NTA2IiBoZWlnaHQ9IjMzLjUyNzkxMjQiIHJ4PSIxLjA0NTAyNTg0Ij48L3JlY3Q+CiAgICAgICAgICAgICAgICAgICAgPHJlY3QgaWQ9IlJlY3RhbmdsZSIgZmlsbD0iI0RGODc2OCIgeD0iMTkuMTM5NjY3NCIgeT0iMCIgd2lkdGg9IjE0LjM1NDc1MDYiIGhlaWdodD0iMTQuMzY5MTA1MyIgcng9IjEuMDQ1MDI1ODQiPjwvcmVjdD4KICAgICAgICAgICAgICAgICAgICA8cmVjdCBpZD0iUmVjdGFuZ2xlIiBmaWxsPSIjRkZGMDdDIiB4PSIxOS4xMzk2Njc0IiB5PSIxOS4xNTg4MDcxIiB3aWR0aD0iMTQuMzU0NzUwNiIgaGVpZ2h0PSIxNC4zNjkxMDUzIiByeD0iMS4wNDUwMjU4NCI+PC9yZWN0PgogICAgICAgICAgICAgICAgICAgIDxsaW5lIHgxPSIxNC4yMzUxMjc2IiB5MT0iNy4wNjQ4MTAxMSIgeDI9IjE5LjAyMDA0NDUiIHkyPSI3LjA2NDgxMDExIiBpZD0iTGluZSI+PC9saW5lPgogICAgICAgICAgICAgICAgICAgIDxsaW5lIHgxPSIyNi4xOTc0MTk4IiB5MT0iMTQuMjQ5MzYyOCIgeDI9IjI2LjE5NzQxOTgiIHkyPSIxOS4wMzkwNjQ1IiBpZD0iTGluZSI+PC9saW5lPgogICAgICAgICAgICAgICAgICAgIDxsaW5lIHgxPSIxNC4yMzUxMjc2IiB5MT0iMjYuNDYzMTAyMyIgeDI9IjE5LjAyMDA0NDUiIHkyPSIyNi40NjMxMDIzIiBpZD0iTGluZSI+PC9saW5lPgogICAgICAgICAgICAgICAgPC9nPgogICAgICAgICAgICAgICAgPGxpbmUgeDE9IjM2LjAwNzI1MzUiIHkxPSIxMy4yOTE0MjI0IiB4Mj0iMzYuMDA3MjUzNSIgeTI9IjAuMTE5NzQyNTQ0IiBpZD0iTGluZS0yIj48L2xpbmU+CiAgICAgICAgICAgICAgICA8bGluZSB4MT0iNzAuODEzNzUyOCIgeTE9IjM1LjkyMjc2MzMiIHgyPSI1OC45MiIgeTI9IjM1Ljg4IiBpZD0iTGluZS0yIj48L2xpbmU+CiAgICAgICAgICAgICAgICA8bGluZSB4MT0iMTMuMTU4NTIxMyIgeTE9IjM1LjkyMjc2MzMiIHgyPSIwLjM2IiB5Mj0iMzUuODgiIGlkPSJMaW5lLTIiPjwvbGluZT4KICAgICAgICAgICAgICAgIDxsaW5lIHgxPSIzNiIgeTE9IjcxLjYzODc5NiIgeDI9IjM2LjAwNjQ5OTMiIHkyPSI1OC43OTM1ODkyIiBpZD0iTGluZS0yIj48L2xpbmU+CiAgICAgICAgICAgIDwvZz4KICAgICAgICA8L2c+CiAgICA8L2c+Cjwvc3ZnPg==&style=for-the-badge
[syl-project-url]: https://github.com/startyourlab/r-project-template
[twitter-shield]: https://img.shields.io/badge/Twitter-Ask%20a%20question-1DA1F2?logo=twitter&url=https%3A%2F%2Ftwitter.com%2Fstartyourlab
[twitter-url]: https://twitter.com/intent/tweet?text=Question%20about%20R%20Project%20Template%20for%20@startyourlab&url=https%3A%2F%2Fgithub.com%2Fstartyourlab%2Fr-project-template
[stackoverflow-shield]: https://img.shields.io/badge/Stack%20Overflow-Ask%20a%20question-F48024?logo=stackoverflow
[stackoverflow-url]: https://stackoverflow.com/questions/ask?tags=startyourlab
