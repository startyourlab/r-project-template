source("renv/activate.R")
#### -- Consistent File Downloads -- ####
if(.Platform$OS.type == "windows") {
  options(
    download.file.method = "wininet"
  )
} else {
  options(
    download.file.method = "libcurl"
  )
}

#### -- Set CRAN -- ####
options(
  repos=c("https://cran.rstudio.com/")
)

#### -- Factors Are Not Strings -- ####
options(
  stringsAsFactors = FALSE
)

#### -- Display -- ####
options(
  digits = 12, # number of significant digits to show by default
  width = 80 # console width
)

#### -- Time Zone -- ####
if (Sys.getenv("TZ") == "") Sys.setenv("TZ" = Sys.timezone())
if (interactive()) {
  message("Session Time: ", format(Sys.time(), tz = Sys.getenv("TZ"), usetz = TRUE))
}

#### -- Session -- ####
.First <- function() {
  if (interactive()) {
    cat("\n")
    utils::timestamp("", prefix = paste("##------ [", getwd(), "] ", sep = ""))
    cat("\nSuccessfully loaded .Rprofile at", base::date(), "\n")
    cat("\n")
    cat("For more information about this project template, go to:\n")
    cat("https://github.com/startyourlab/r-project-template\n")
  }
}

if (interactive()) {
  message("Session Info: ", utils::sessionInfo()[[4]])
  message("Session User: ", Sys.info()["user"])
}

options(
  prompt = "R > ",
  continue = "... "
)

#### -- Dev Tools -- ####
if (interactive()) {
  library(fs)
  library(devtools)
}

