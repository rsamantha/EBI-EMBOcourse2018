FROM rocker/tidyverse:latest
MAINTAINER "Samantha Riccadonna" <samantha.riccadonna@fmach.it>

# Installing dev version of packages needed for netcdf R package
RUN apt-get update -qq\
  && apt-get install -y --no-install-recommends \
    libnetcdf-dev \    #needed for netCFD package needed for mzR
    mesa-common-dev \  #needed for xcms
    libglu1-mesa-dev \ #needed for xcms
    libudunits2-dev \  #needed for plotly (udunits2)
    libxt-dev \        #needed for plotly (sf)
    libgdal-dev        #needed for plotly (sf)
  
# Installing required packages
RUN install2.r --error \
    -r "https://cran.rstudio.com" \
    -r "http://www.bioconductor.org/packages/release/bioc" \  
    --deps TRUE \
    mzR \
    xcms \
    CAMERA \ 
    ptw \ 
    scales \ 
    plotly \ 
    markdown \
    BioMark \ 
    shiny \
# Installing packages for data handling and visualization
    FactoMineR \
    factoextra \ 
    RColorBrewer 

#Installing EBI-EMBO course related packages
RUN installGithub.r pietrofranceschi/LCMSdemo  

# Clean
RUN apt-get clean \
  && rm -rf /tmp/downloaded_packages/* \
  && rm -rf /var/lib/apt/lists/*
