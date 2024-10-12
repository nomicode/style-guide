# Use the base Ubuntu image
FROM mcr.microsoft.com/devcontainers/base:ubuntu

# Update apt sources list, install npm, and use npm to install Yarn globally
RUN apt-get update && \
    apt-get install -y --no-install-recommends curl gnupg && \
    curl -sL https://deb.nodesource.com/setup_22.x | bash - && \
    apt-get install -y nodejs && \
    npm install --global yarn && \
    # Cleanup
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
