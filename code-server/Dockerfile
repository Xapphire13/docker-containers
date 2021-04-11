FROM codercom/code-server:latest

# Persistant user settings
WORKDIR /home/coder
RUN mkdir -p .local/share/code-server
RUN chown -R coder /home/coder/.local
VOLUME /home/coder/.local/share/code-server

# Fix ASAR bug
RUN sudo ln -s /usr/lib/code-server/lib/vscode/node_modules /usr/lib/code-server/lib/vscode/node_modules.asar

# Install nodejs and npm
RUN curl -fsSL https://deb.nodesource.com/setup_14.x | sudo -E bash -
RUN sudo apt-get install -y nodejs
