# VirusTotal-API-V3-Postman

In Postman, you can dynamically update the IP address used in your requests by utilizing a Pre-request Script. This script allows you to set an IP address as an environment variable before each request is sent. For example, you can maintain a list of IP addresses and use JavaScript logic to select one (e.g., randomly or in sequence) and assign it to an environment variable like ip. By using {{ip}} as a placeholder in your request URL, Postman will automatically substitute it with the dynamically selected IP address. This method enhances flexibility and automation in testing scenarios where multiple IP addresses need to be queried.

Download the Json file and Import it to Postman!
