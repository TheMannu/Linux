### HTTP Status Codes Overview

#### 1. Informational Responses (100–199)
- **100 Continue**: The initial part of a request has been received and the client can continue with the request.
- **101 Switching Protocols**: The server switches protocols as requested by the client.
- **102 Processing**: Indicates that the server has received and is processing the request but no response is available yet.

#### 2. Successful Responses (200–299)
- **200 OK**: The request was successful, and the server returned the requested resource.
- **201 Created**: The request succeeded, and a new resource was created.
- **204 No Content**: The server successfully processed the request, but there is no content to send in the response.

#### 3. Redirection Messages (300–399)
- **301 Moved Permanently Redirected**: The resource has been moved to a new URL.
- **302 Found (Temporary Redirect)**: The resource is temporarily available at a different URL.
- **304 Not Modified**: The requested resource has not been modified since the last request.

#### 4. Client Error Responses (400–499)
- **400 Bad Request**: The server couldn't understand the request due to invalid syntax.
- **401 Unauthorized**: Authentication is required to access the requested resource.
- **403 Forbidden**: The client does not have permission to access the resource.
- **404 Not Found**: The requested resource could not be found.
- **405 Method Not Allowed**: The HTTP method used is not allowed for the requested resource.

#### 5. Server Error Responses (500–599)
- **500 Internal Server Error**: The server encountered an unexpected condition.
- **501 Not Implemented**: The server does not support the functionality required to fulfill the request.
- **502 Bad Gateway**: The server received an invalid response from an upstream server.
- **503 Service Unavailable**: The server is not ready to handle the request, often due to being overloaded.
- **504 Gateway Timeout**: The server did not receive a timely response from an upstream server.

---

### Troubleshooting Techniques for HTTP Errors

#### Windows Troubleshooting

1. **Use Browser Developer Tools**
   - Press `F12` to open the browser developer console.
   - Navigate to the "Network" tab to inspect requests and responses, including HTTP status codes and detailed error messages.
   - This helps diagnose issues like failed resource loading, CORS problems, or network timeouts.

2. **Check Logs**
   - Check the browser console for JavaScript errors.
   - If running a web server, review server logs (e.g., IIS logs located at `C:\inetpub\logs\LogFiles`) for any clues.

3. **Clear Cache**
   - Often, outdated cached resources cause issues. Clearing the browser cache might fix 304 "Not Modified" errors.
   - Use `Ctrl + Shift + R` to hard-refresh the page.

4. **Check DNS Settings**
   - Use `ipconfig /flushdns` in Command Prompt to flush DNS, which resolves DNS-related issues.

#### Linux Troubleshooting

1. **Inspect HTTP Requests with Curl**
   - Use `curl -I <URL>` to inspect HTTP headers and status codes for a given URL:
     ```bash
     curl -I http://example.com
     ```
   - You can also use `curl -v` for verbose output to see the entire transaction, including headers.

2. **Use Log Files**
   - **Apache Logs**: `/var/log/apache2/error.log` or `/var/log/apache2/access.log`.
   - **Nginx Logs**: `/var/log/nginx/error.log` or `/var/log/nginx/access.log`.
   - Check logs for errors, especially if the server is returning 500 errors.

3. **Network Tools**
   - Use `ping` or `traceroute` to verify connectivity to a server.
   - Example:
     ```bash
     ping google.com
     traceroute google.com
     ```

4. **Check Service Status**
   - For Linux web servers, ensure the server is running:
     ```bash
     systemctl status apache2  # For Apache
     systemctl status nginx    # For Nginx
     ```

5. **Firewall & Proxy Settings**
   - Verify firewall settings with `ufw` or `iptables` to ensure requests aren't being blocked:
     ```bash
     sudo ufw status
     sudo iptables -L
     ```

6. **Analyze with `netstat` or `ss`**
   - Use `netstat` or `ss` to examine open ports and active connections. This helps identify if the web server is listening on the correct port:
     ```bash
     sudo netstat -tuln
     sudo ss -tuln
     ```

7. **DNS Troubleshooting**
   - Use `nslookup` or `dig` to diagnose DNS issues:
     ```bash
     nslookup example.com
     dig example.com
     ```

8. **Check Server Load**
   - Use commands like `top`, `htop`, or `vmstat` to ensure the server isn’t overloaded, which could cause 503 "Service Unavailable" errors.
