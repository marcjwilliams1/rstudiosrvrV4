Bootstrap: docker
From: rocker/r-ver:4.0.3

%post
  export S6_VERSION=v1.21.7.0
  export RSTUDIO_VERSION=1.2.5042
  export PATH=/usr/lib/rstudio-server/bin:$PATH
  /rocker_scripts/install_rstudio.sh
  /rocker_scripts/install_pandoc.sh

  apt-get update && apt-get install -y --no-install-recommends apt-utils

  /rocker_scripts/install_tidyverse.sh
