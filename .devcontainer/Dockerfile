FROM perl:latest

# Update and install dependencies
RUN apt-get update && apt-get install -y \
    build-essential \
    curl \
    less \
    vim \
    git

# Set up CPAN and install commonly used modules
RUN cpan App::cpanminus
RUN cpanm \
    Mojolicious \
    DBI \
    DBD::mysql \
    LWP::UserAgent \
    JSON::XS

# Set the default shell to bash
ENV SHELL=/bin/bash

# Expose ports
EXPOSE 3000

# Set the working directory
WORKDIR /workspace
