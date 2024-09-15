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
