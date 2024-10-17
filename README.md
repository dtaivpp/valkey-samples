# Valkey Docker Compose Samples

This repo contains a few sample configurations used for testing Valkey. These are all single node configurations. The `valkey-cluster` creates several Valkey instances on one machine to maximize the throughput of Valkey by running in clustered mode. These were used for [this blog](https://valkey.io/blog/testing-the-limits) which provides much more context.

# Setup

1. Copy `sample.env` to a `.env` file: `cp sample.env .env`
2. Modify the values in the `.env` file
    - For a reasonably secure password you can use `head -16 /dev/urandom | openssl sha1` to generate the password
    - The `NODE_IP` should be set to the IP of the host you are running on
3. `docker compose -f <SETUP FILE> up -d` to start your desired configuraition 

