# HTTP response status codes
HTTP response status codes are issued by a server in response to a client's request made to the server. They indicate whether a specific HTTP request has been successfully completed. Here are the main categories of HTTP response status codes:

* # Informational responses (100–199)
### 100 Continue
This interim response indicates that the client should continue the request or ignore the response if the request is already finished.

### 101 Switching Protocols
This code is sent in response to an Upgrade request header from the client and indicates the protocol the server is switching to.

### 102 Processing Deprecated
This code was used in WebDAV contexts to indicate that a request has been received by the server, but no status was available at the time of the response.

### 103 Early Hints
This status code is primarily intended to be used with the Link header, letting the user agent start preloading resources while the server prepares a response or preconnect to an origin from which the page will need resources.

* # Successful responses (200–299)
### 200 OK
The request has succeeded.

### 201 Created
The request has been fulfilled and a new resource has been created.

### 204 No Content
The server successfully processed the request and is not returning any content.

* # Redirection Messages (300–399)
301 Moved Permanently: The requested resource has been assigned a new permanent URI.

302 Found: The requested resource resides temporarily under a different URI.

304 Not Modified: There is no need to retransmit the resource, as it has not been modified since the previous request.

* # Client Error Responses (400–499)
### 400 Bad Request
The server could not understand the request due to invalid syntax.

### 401 Unauthorized
The client must authenticate itself to get the requested response.

### 403 Forbidden
The client does not have access rights to the content.

### 404 Not Found
The server can not find the requested resource.

* # Server Error Responses (500–599)
### 500 Internal Server Error
The server has encountered a situation it does not know how to handle. This error is generic, indicating that the server cannot find a more appropriate 5XX status code to respond with.

### 501 Not Implemented
The request method is not supported by the server and cannot be handled. The only methods that servers are required to support (and therefore that must not return this code) are GET and HEAD.

### 502 Bad Gateway
This error response means that the server, while working as a gateway to get a response needed to handle the request, got an invalid response.

### 503 Service Unavailable
The server is not ready to handle the request. Common causes are a server that is down for maintenance or that is overloaded. Note that together with this response, a user-friendly page explaining the problem should be sent. This response should be used for temporary conditions and the Retry-After HTTP header should, if possible, contain the estimated time before the recovery of the service. The webmaster must also take care about the caching-related headers that are sent along with this response, as these temporary condition responses should usually not be cached.

### 504 Gateway Timeout
This error response is given when the server is acting as a gateway and cannot get a response in time.

### 505 HTTP Version Not Supported
The HTTP version used in the request is not supported by the server.

### 506 Variant Also Negotiates
The server has an internal configuration error: during content negotiation, the chosen variant is configured to engage in content negotiation itself, which results in circular references when creating responses.

### 507 Insufficient Storage (WebDAV)
The method could not be performed on the resource because the server is unable to store the representation needed to successfully complete the request.

### 508 Loop Detected (WebDAV)
The server detected an infinite loop while processing the request.

### 510 Not Extended
The client request declares an HTTP Extension (RFC 2774) that should be used to process the request, but the extension is not supported.

### 511 Network Authentication Required
Indicates that the client needs to authenticate to gain network access.

These status codes help in identifying what went wrong with a request or whether it was successfully processed, making them essential for debugging and understanding web interactions.