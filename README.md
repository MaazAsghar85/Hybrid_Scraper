
# Hybrid Scraper

## Overview

Welcome to **Hybrid Scraper**, a project designed to scrape data efficiently using Docker containers for both client and server. Follow the setup instructions below to get started.

---

## Prerequisites

Ensure you have the following installed before proceeding:

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

---

## Clone the Repository

First, clone the repository to your local machine:

```bash
git clone git@github.com:MaazAsghar85/Hybrid_Scraper.git
```

Navigate into the project directory:

```bash
cd Hybrid_Scraper
```

---

## Setup Instructions

The setup involves running two terminals: one for the **client** and one for the **server**.

### 1. Start the Server

In **Terminal 1**, execute the following commands to build and start the Docker containers:

```bash
docker-compose build
docker-compose up
```

Once the containers are up, you should see the output:

```
Welcome to instaRS
```

### 2. Connect to the Client

In **Terminal 2**, run the following command to access the client container:

```bash
docker exec -it cpp_client /bin/bash
```

Inside the client container, start the client application:

```bash
./instaRS
```

If successful, you should see the following output:

```
Connected to server
instaRS>>
```

---

## Expected Outputs

- **Terminal 1 (Server)**: `Welcome to instaRS`
- **Terminal 2 (Client)**: `Connected to server` followed by `instaRS>>`

---

## Troubleshooting

- Ensure that Docker is running on your machine.
- Make sure you run `docker-compose build` before `docker-compose up` to avoid missing dependencies.

---

## Contact

For questions, please contact **Maaz Asghar** at [maazasghar@example.com](mailto:maazasghar85@gmail.com).
