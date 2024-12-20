﻿# Peer-to-Peer-Sharing
# BitTorrent File Sharing System

This repository contains a custom BitTorrent-like system for file sharing, including a Tracker, Seeder, and Peers. The project demonstrates the peer-to-peer (P2P) file-sharing protocol and allows users to upload, download, and manage files efficiently within a local network.

---

## Table of Contents
- [Features](#features)
- [System Requirements](#system-requirements)
- [Installation Guide](#installation-guide)
  - [Setting Up Devices](#setting-up-devices)
  - [Required Tools](#required-tools)
- [Usage Instructions](#usage-instructions)
  - [Creating Torrent Files](#creating-torrent-files)
  - [Uploading Files](#uploading-files)
  - [Downloading Files](#downloading-files)
  - [Viewing Torrent Information](#viewing-torrent-information)
- [License](#license)

---

## Features
- **Tracker**: Coordinates communication between Seeder and Peers.
- **Seeder**: Shares files with requesting Peers.
- **Peers**: Download files from Seeder and potentially other Peers.
- **LAN Support**: Operates within a local network for fast and secure file sharing.
- **CLI Commands**: Manage torrent files and file-sharing processes using intuitive CLI commands.

---

## System Requirements
- Minimum 4 devices:
  - **1 device** as a Tracker
  - **1 device** as a Seeder
  - **2 devices** as Peers for downloading files
- All devices must be connected to the **same LAN**.

---

## Installation Guide

### Setting Up Devices
Ensure you have at least 4 devices:
1. **Tracker**: Manages the sharing process.
2. **Seeder**: Uploads files to share.
3. **Peers**: Downloads files shared by Seeder.

### Required Tools
Install the following tools on all devices:
- **Python**
- **Docker**
- **Pip**
- **MySQL**

Use your package manager or installer to set up these tools.

---

## Usage Instructions

### Running the System
1. **Start Tracker**: Launch the tracker service to coordinate file sharing.
2. **Start CLI and Nodaemon**: Ensure the system is ready for user commands.

---

### Creating Torrent Files
To share a file, create a `.torrent` file for the source directory:
bitorrent create [-o | --output : filename] [source directory]
Uploading Files
To upload a file, Seeder runs the following command:
bitorrent upload [-p | -port : port number] [.torrent file name]
Downloading Files
To download a file, a Peer must have the .torrent file and run:
bitorrent download [-p | -port : port number] [.torrent file name]
Viewing Torrent Information
To show information about a specific .torrent file:
bitorrent show [-f | --file : filename]
To display a list of Peers in a torrent:
bitorrent show [-i | --info : info hash]
To display general torrent information:
bitorrent show

