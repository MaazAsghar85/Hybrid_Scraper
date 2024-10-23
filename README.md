
# Hybrid Scraper

## Overview

Welcome to **Hybrid Scraper**, a command-line based project designed to scrape data efficiently using Docker containers for both client and server. This tool is specifically designed for scraping Instagram user data, including profile picture (PFP), posts media, posts text, reels links, reels text, highlights, followers, followings, and detailed data of followers and followings.

Follow the setup instructions below to get started.

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

## Available Features

With **Hybrid Scraper**, you can download:

- Instagram user's profile picture (PFP)
- Posts media (images and videos)
- Posts text (captions)
- Reels links and texts
- Instagram highlights
- Followers list
- Followings list
- Detailed data of followers and followings

---

## Command-line Usage

The **Hybrid Scraper** app provides a rich set of command-line functionalities for browser and Instagram data scraping. Below are the available commands:

### Browser and Page Management:
- `lb` - Launch a new browser
- `lp` - Launch a new page
- `cb [browser num]` - Close browser (default: active browser)
- `cp [page num]` - Close page (default: active page)
- `sap [page num]` - Set active page
- `sab [browser num]` - Set active browser
- `lsb` - List all browsers
- `lsp` - List all pages

### Session and Environment Management:
- `senv` - Set environment
- `lenv` - Load environment
- `scook [filename]` - Save browser cookies to a file
- `lcook [filename]` - Load browser cookies from a file
- `set sleep [num]` - Sets the sleep for the current session

### Instagram Functionalities:
- `login [user] [pass]` - Log in to Instagram with provided credentials
- `search [username]` - Search specified Instagram user
- `goto [link]` - Navigate to specified URL

### Data Management Commands:
- `dump [option]` - Download user data based on the option:
  - `-max` - All user data including Followers/Following
  - `-a` - All user data excluding Followers/Following
  - `-t` - All text-related data
  - `-m` - All media-related data
  - `-p` - Profile Picture only
  - `-u` - User Data only
  - `-pt` - Post text (Captions, Comments, etc)
  - `-pm` - Post Media (Images)
  - `-r` - Reels
  - `-h` - Highlights
  - `-fr [num]` - Number of Followers usernames, e.g., 100
  - `-fg [num]` - Number of Following usernames, e.g., 100
  - `-fru` - User Data of extracted Followers
  - `-fgu` - User Data of extracted Following
  - `-frp` - Profile Pic of extracted Followers
  - `-fgp` - Profile Pic of extracted Following

### Utility Commands:
- `ss [filename]` - Save screenshot of active page in the given filename
- `--list` - List all commands
- `quit` - Close instaRS console

---

## Troubleshooting

- Ensure that Docker is running on your machine.
- Make sure you run `docker-compose build` before `docker-compose up` to avoid missing dependencies.
- **Important**: The app may not download some data if Instagram updates their platform or makes changes to their data structure. If you encounter any issues with missing data, feel free to contact me.

---

## Contact

For questions or issues, please contact **Maaz Asghar** at [maazasghar85@gmail.com](mailto:maazasghar85@gmail.com).

---
