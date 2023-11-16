# Fork of SToPA Toolkit Shiny app for Michigan State datathon participants

This is a fork of the [official repository for the SToPA tookit Shiny app](https://github.com/WilliamCipolli/QsideProject), currently hosted [here](http://stopadata.qsideinstitute.org).

# Fork information

This fork is for testing local development of the Shiny app on Michigan State University's high-performance computing cluster in anticipation of 2023 Datathon4Justice.

# Getting started

## Using RStudio (recommended)

1. Clone this repository to your desired location with `git clone https://github.com/cgross95/QsideProject.git`
2. Start an RStudio session.
    1. If you can access MSU ICER resources, consider starting an [OnDemand RStudio job](https://ondemand.hpcc.msu.edu).
    2. Otherwise, download and install R and RStudio following [Posit's instructions](https://posit.co/download/rstudio-desktop/). 
4. Open the file `app/ui.R` in RStudio.
5. If necessary, install the required dependencies in R using the pop up at the top of the file editor.
6. Click the "Run App" button at the top of the file editor.

## Using R without RStudio

1. Clone this repository to your desired location with `git clone https://github.com/cgross95/QsideProject.git`
2. Start R from the command line in the directory where you cloned the repository.
    1. If you can access MSU ICER resources, consider using `R/4.1.2` with the commands `module purge; module load GCC/11.3.0  OpenMPI/4.1.4 R/4.2.1; R`
    2. Otherwise, download and install R following [the official directions for your operating system](https://cran.rstudio.com/).
3. Install the necessary depedencies. This includes (but may not be limited to)
    ``` R
    install.packages(shiny, shinyalert, shinyjs, shinymeta, shinythemes, shinyAce, shinyBS, DT, zip, tidyverse, tigris, sf, tidycensus, labelled, openxlsx, lubridate, hms)
    ```
4. Run the command `shiny::startApp(".")`
5. Access the URL provided in the output through your web browser. **Note**: if you are running from a command line on a remote machine (like an MSU ICER development node), you will need to forward the port that the app is running on. See [this documentation page](https://docs.icer.msu.edu/2023-03-27_LabNotebook_Jupyter_port-forward_servers/) for an example.
