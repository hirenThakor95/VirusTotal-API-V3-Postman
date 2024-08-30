# VirusTotal-API-V3-Postman

This repository contains a Postman collection for interacting with the VirusTotal API v3. Currently, it includes functionality to retrieve IP address reports. More API functions will be added over time.

## Features

- **Retrieve IP Address Report:** Use the VirusTotal API v3 to get detailed information about a specific IP address.

## Dynamic IP Address Handling

In Postman, you can dynamically update the IP address used in your requests by utilizing a Pre-request Script. This script allows you to set an IP address as an environment variable before each request is sent. For example, you can maintain a list of IP addresses and use JavaScript logic to select one (e.g., randomly or in sequence) and assign it to an environment variable like `ip`. By using `{{ip}}` as a placeholder in your request URL, Postman will automatically substitute it with the dynamically selected IP address. This method enhances flexibility and automation in testing scenarios where multiple IP addresses need to be queried.

## Setup Instructions

1. **Download the JSON File:**
   - Download the provided Postman collection JSON file from this repository.

2. **Import into Postman:**
   - Open Postman.
   - Click on "Import" in the top-left corner.
   - Select the downloaded JSON file to import the collection.

3. **Set Up Environment:**
   - Create a new environment in Postman or use an existing one.
   - Add a variable named `apikey` and set its value to your VirusTotal API key.
   - Add a variable named `ip` and set its initial value to an IP address you want to query.

4. **Pre-request Script:**
   - In the request, go to the "Pre-request Script" tab.
   - Add JavaScript code to dynamically select an IP address and set it as the `ip` variable.

   Example:
   ```javascript
   const ipAddresses = ["192.168.1.1", "8.8.8.8", "8.8.4.4"];
   const selectedIp = ipAddresses[Math.floor(Math.random() * ipAddresses.length)];
   pm.environment.set("ip", selectedIp);
