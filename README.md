# R Project Template using RStudio

This is a template to begin analysis projects in R Studio.

## Prerequisites

### Local Applications

To use this template, you must have the following installed locally:

- Git
- R
- RStudio

### R Packages

You will have an even better experience using this template if you also
install standard system packages for working with R to do analysis:

- devtools
- fs
- config
- knitr

Simply use `install.packages("devtools")`, replacing `devtools` with
the other package names for each installation.

## Installation

To use this template, click the green **Use this template** button or you can [click
here](https://github.com/aridyckovsky/r-project-template/generate) to generate
your project. It will ask you to name the repository and add a description (optional).

Once the repository is generated, you will be redirected to your new repository.

## Usage

With your new repository, it's time to start using it. Click the green **Code** button
and copy the HTTPS-based URL (just click the clipboard icon!). Then, in your terminal,
run the command

```
git clone https://github.com/username/repository.git
```

making sure that you change `username` for your GitHub username
and `repository` for the name of your new repository.

You'll need to rename the following files with your own names:

- `template.Rproj`, changing `template` to your repository name
- `notebook-template.Rmd`, changing `notebook-template` to the notebook
  name that you would like.
- `LICENSE`, replacing the template author's name with your name.

Once files are renamed, it's time to commit these changes as your
first commit to GitHub. From the root of the project directory, run the 
following commands one-at-a-time, in order.

```
git add .
git commit -am "Rename core files"
git push
```

Now that everything is squared away, it's time to start work on your
project. Open the renamed `.Rproj` file in RStudio, and get to it!

## Support

For questions about this template, please contact [Ari Dyckovsky](mailto:aridyckovsky@gmail.com).
