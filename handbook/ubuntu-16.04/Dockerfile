FROM ubuntu:16.04
MAINTAINER Rasmus Villemoes <ravi@prevas.dk>

RUN apt-get -y update
RUN apt-get install -y        \
    apt-utils sudo            \
    bash-completion git make  \
    python-sphinx             \
    sphinx-rtd-theme-common
RUN apt-get clean
RUN rm -rf /var/lib/apt/lists/*

# TBD: Figure out the necessary packages to allow "make latexpdf" to
# build a pdf version. Probably at least these:

  # texlive-latex-base        \
  # texlive-latex-recommended \
  # texlive-fonts-recommended \
  # texlive-latex-extra

# Add non-root user 
RUN useradd -m -s /bin/bash user \
 && echo user ALL=NOPASSWD: ALL > /etc/sudoers.d/user
USER user

WORKDIR /home/user
