FROM mcr.microsoft.com/devcontainers/universal:2-linux
# Install the xz-utils package
RUN apt-get update 
RUN curl -sL https://deb.nodesource.com/setup_16.x | bash - \
    && apt-get install -y nodejs \
    && rm -rf /var/lib/apt/lists/*

RUN npm install -g @vue/cli
WORKDIR /workspace

RUN python3 -m venv /workspace/venv \
    && /workspace/venv/bin/pip install --upgrade pip \
    && /workspace/venv/bin/pip install Flask
