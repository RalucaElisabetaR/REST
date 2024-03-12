# **REST Cheat Sheet**

## **Introduction to REST**
`REST` (**Representational State Transfer**) is an architectural style for designing networked applications. It uses a stateless, client-server, cacheable communications protocol, primarily the HTTP protocol. REST simplifies web services by leveraging existing protocols and conventions, focusing on resources identified by URLs and standard HTTP methods.

## **Core Principles of REST**

### **Client-Server Architecture**
- Separates concerns between client (user interface) and server (data storage).
- Promotes independence and scalability.

### **Statelessness**
- Each request from client to server must contain all the information needed to understand and complete the request. No client context is stored on the server between requests.

### **Cacheability**
- Responses must be defined as cacheable or not. This helps improve performance and scalability.

### **Uniform Interface**
- Simplifies and decouples the architecture, allowing each part to evolve independently.
- **Resource Identification in Requests**: Resources are identified using URIs.
- **Resource Manipulation Through Representations**: When a client has a representation of a resource, it has enough information to modify or delete the resource on the server.
- **Self-descriptive Messages**: Each message includes enough information to describe how to process it.
- **Hypermedia as the Engine of Application State (HATEOAS)**: Clients change state through links provided dynamically by server responses.

### **Layered System**
- The client cannot tell whether it is connected directly to the end server, or an intermediary. This promotes security and scalability.

## **HTTP Methods**
- **`GET`**: Retrieve information about a resource.
- **`POST`**: Create a new resource.
- **`PUT`**: Update an existing resource.
- **`DELETE`**: Remove a resource.
- **`PATCH`**: Apply partial updates to a resource.
- **`OPTIONS`**: Describe the communication options for the target resource.
- **`HEAD`**: Similar to `GET` but without the response body.

## **Status Codes**
- **2xx Success**: `200 OK`, `201 Created`, `204 No Content`
- **3xx Redirection**: `301 Moved Permanently`, `304 Not Modified`
- **4xx Client Error**: `400 Bad Request`, `401 Unauthorized`, `403 Forbidden`, `404 Not Found`, `405 Method Not Allowed`
- **5xx Server Error**: `500 Internal Server Error`, `503 Service Unavailable`

## **Best Practices**
- Use plural nouns for resource names (e.g., `/users`).
- Be consistent with naming conventions.
- Nest resources to represent relationships (e.g., `/users/123/posts`).
- Use HTTP headers for authentication, status codes for responses, and consider caching headers to improve performance.
- Secure APIs using HTTPS and tokens (OAuth, JWT).
- Implement error handling and meaningful status codes.
- Include versioning in the API path (e.g., `/api/v1/resources`).



This document summarizes key REST principles, methods, status codes, and best practices for designing and interacting with RESTful APIs.
