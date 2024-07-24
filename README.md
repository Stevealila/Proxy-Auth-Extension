# Proxy Auth Extension

The **Proxy Auth Extension** is a simple Chrome extension that allows you to configure and authenticate a proxy server directly within the browser. This extension sets up a fixed proxy server and handles authentication using provided credentials.

## Features

- **Fixed Proxy Configuration**: Automatically configures a proxy server for all requests.
- **Authentication Handling**: Supports proxy authentication with username and password.
- **Wide Permissions**: Access to all URLs and web requests, unlimited storage.

## Prerequisites

- Google Chrome or Chromium browser.

## Getting Started

1. **Clone the Repository**

   Clone this repository to your local machine:

   ```bash
   git clone https://github.com/Stevealila/Proxy-Auth-Extension.git
   ```

   **Create the Extension**

   Run the `create_proxy_auth_extension` function to generate the extension ZIP file. Provide the necessary proxy details:

   ```python
   from proxy_auth_extension import create_proxy_auth_extension
   
   proxy_host = "your.proxy.host"
   proxy_port = 1234
   proxy_username = "your_username"
   proxy_password = "your_password"
   
   proxy_auth_extension = create_proxy_auth_extension(proxy_host, int(proxy_port), username, password)
   
   # Example usage in Selenium
   chrome_options = Options()
   chrome_options.add_extension(proxy_auth_extension)
   chrome_options.add_argument('--no-sandbox')
   chrome_options.add_argument('--disable-dev-shm-usage')
   chrome_options.add_argument('--disable-blink-features=AutomationControlled')
   ```

   This function will create a `proxy_auth_extension.zip` file with the extension files. You can clear the local file after your script has completed running `os.remove(proxy_auth_extension)`.

   
