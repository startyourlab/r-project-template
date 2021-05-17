# R Project Template

This is a template repository for **using R with a team**. Use this template to leverage a shared set of configurations optimized for teams developing projects in R.

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

For questions about this template, please contact [Start Your Lab](https://www.startyourlab.com/community/support).
