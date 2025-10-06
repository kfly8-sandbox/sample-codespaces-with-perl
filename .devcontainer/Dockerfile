FROM perl:5.42.0-slim

# Install locales and generate en_US.UTF-8
RUN apt-get update && \
    apt-get install -y locales && \
    echo "en_US.UTF-8 UTF-8" > /etc/locale.gen && \
    locale-gen en_US.UTF-8 && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Set locale environment variables
ENV LANG=en_US.UTF-8 \
    LC_ALL=en_US.UTF-8

# Install Carton
RUN cpanm Carton

# Set working directory
WORKDIR /workspaces/sample-codespaces-with-perl

# Copy cpanfile and install dependencies
COPY cpanfile ./
RUN carton install
