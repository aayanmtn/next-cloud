# Nextcloud Docker Compose Setup

This repository provides an easy-to-use setup for deploying [Nextcloud](https://nextcloud.com/) with Docker Compose. The setup includes a Nextcloud container, a MariaDB database, and persistent data storage.

## Prerequisites

Before you begin, ensure you have the following installed:

- **Docker**: [Install Docker](https://docs.docker.com/get-docker/)
- **Docker Compose**: [Install Docker Compose](https://docs.docker.com/compose/install/)

### Install Docker

Run the following commands to install Docker on a **Linux** system:

```bash
# Update the apt package index
sudo apt-get update

# Install dependencies
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common

# Add Docker’s official GPG key
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

# Set up the stable repository
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"

# Install Docker
sudo apt-get update
sudo apt-get install docker-ce
