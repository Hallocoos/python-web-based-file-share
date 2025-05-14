# File Sharing with Python HTTP Server

## Overview

This guide explains how to use Python's built-in HTTP server to share files in the current directory over a local network. This is a quick and simple method for sharing files without additional software.

## Prerequisites

* Python 3.x installed
* Local network access

## Usage

1. **Navigate to the directory you want to share:**

   ```bash
   cd /path/to/your/directory
   ```

2. **Start the HTTP server:**

   ```bash
   python -m http.server 8000
   ```

   This starts a server on port `8000`. You can replace `8000` with any available port if needed.

3. **Find your local IP address:**

   * On Windows:

     ```powershell
     ipconfig
     ```
   * On macOS/Linux:

     ```bash
     ifconfig
     ```

   Locate the IP address under your active network adapter (e.g., `192.168.1.10`).

4. **Access the server from another device:**
   Open a web browser on any device connected to the same network and enter:

   ```
   http://<your-ip-address>:8000
   ```

   Replace `<your-ip-address>` with the IP address you found earlier.

   Example:

   ```
   http://192.168.1.10:8000
   ```

## Security Considerations

* This method is only intended for local network sharing, not for public access.
* Avoid running this on unsecured networks.
* Press `CTRL + C` to stop the server when finished.

## Troubleshooting

* **Port Already in Use:** Choose another port:

  ```bash
  python -m http.server 9000
  ```
* **Firewall Blocking Access:** Ensure your firewall allows incoming connections on the specified port.

## Notes

* You have full read access to the directory where the server was started.
* If you need write access, consider using `SimpleHTTPServerWithUpload` (not included in this tutorial).

## Stopping the Server

To stop the server, press `CTRL + C` in the terminal where it's running.

---

Now you can easily share files across your local network using just Python's built-in capabilities!

## README.md generated with ChatGPT
