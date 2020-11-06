Bootstrap: docker
From: rocker/r-ver:4.0.3

%files
  /rocker_scripts

%post
  export S6_VERSION=v1.21.7.0
  export RSTUDIO_VERSION=1.2.5042
  export PATH=/usr/lib/rstudio-server/bin:$PATH
  /rocker_scripts/install_rstudio.sh
  /rocker_scripts/install_pandoc.sh

  apt-get update
  apt-get install -y apt-utils

  set -e
  apt-get update -qq && apt-get -y --no-install-recommends install \
      libxml2-dev \
      libcairo2-dev \
      libgit2-dev \
      default-libmysqlclient-dev \
      libpq-dev \
      libsasl2-dev \
      libsqlite3-dev \
      libssh2-1-dev \
      unixodbc-dev && \
    rm -rf /var/lib/apt/lists/*

  #/rocker_scripts/install_tidyverse.sh
