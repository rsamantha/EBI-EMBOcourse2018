# EBI-EMBO course 2018 by Pietro Franceschi and Samantha Riccadonna

Extends the docker image [rocker/tidyverse](https://hub.docker.com/r/rocker/tidyverse), providing the packages and data needed for our lesson for the EBI-EMBO metabolomics course 2018.

## Available Tags/Versions

- latest: GitHub snapshot

## Quickstart

1. Download the latest version:

   `docker pull rsamantha/ebi-embocourse2018`

2. Run an instance of the image, mounting the host directory:

   `docker run -d -p 8787:8787 rsamantha/ebi-embocourse2018`

3. Using a web browser visit that address appended with the port (8787), e.g.:

  `localhost:8787`

4. You can now login using default username (rstudio) and password (rstudio).

####Credits: thanks to Davide Albanese and its experience with compmetagen dockers.
