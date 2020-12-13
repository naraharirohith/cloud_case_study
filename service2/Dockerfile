# Node image
FROM node:latest

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
    && rm -rf /var/lib/apt/lists/*
    
# Install the packages
pkg install nodejs
npm install -g truffle@5.0.2
sudo apt install ganache
RUN npm install -g --save ethereumjs-testrpc

WORKDIR /usr/src/app

COPY . .

# Expose port
EXPOSE 8545

# Start TestRPC
ENTRYPOINT ["testrpc"]
