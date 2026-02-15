# Tronbyt server-docker-compose files
[Demo Server](https://tronbyt.clodhost.com/auth/register)

This is a minimal Docker setup to run the Tronbyt server.  For the full code and details of the server go to the [server](https://github.com/tronbyt/server) repo.

## 🚀 Quick Start

```bash
git clone https://github.com/tronbyt/server-docker-compose.git tronbyt-server
cd tronbyt-server
docker-compose up -d
```
Wait up to 60 seconds for the server to come up. It has to download the apps repo on first boot.

[Video Walkthrough on Raspberry PI](https://youtu.be/ZyE1IC97dVw)

## 🥧 Raspberry Pi Automated Setup

For a one-command installation on Raspberry Pi, use the setup script:

```bash
curl -fsSL https://raw.githubusercontent.com/tronbyt/server-docker-compose/main/rpi_setup.sh | bash
```

Or download and run manually:

```bash
wget https://raw.githubusercontent.com/tronbyt/server-docker-compose/main/rpi_setup.sh
chmod +x rpi_setup.sh
./rpi_setup.sh
```

This script will:
- Install Docker and Docker Compose if not present
- Clone the repository
- Start the containers
- Wait for the server to be ready (checking for HTTP 200/303 responses)
- Display access URLs

