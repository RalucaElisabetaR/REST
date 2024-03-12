# REST: Representational State Transfer

REST, or Representational State Transfer, is an architectural style designed for networked applications. It utilizes a stateless, client-server, cacheable communications protocol, with the HTTP protocol being the most commonly used medium. REST is favored in web services development due to its straightforward approach and reliance on the existing infrastructure and capabilities of the internet's HTTP. This design choice allows REST to achieve its goals without the need for inventing new standards, frameworks, or technologies.

## Core Concepts of REST

The essence of REST revolves around **resources**, which are identified by URLs, and the **methods** defined by the HTTP protocol to interact with these resources. RESTful applications leverage HTTP requests to:

- **Post data** (create or update resources),
- **Read data** (e.g., execute queries), and
- **Delete data**,

effectively treating web services as a resource platform where create, read, update, and delete (CRUD) operations can be executed.

## REST Principles
- **Client-Server Architecture**: Separate concerns between the client (front end) and the server (back end).
- **Stateless**: Each request from client to server must contain all information needed to complete the request.
- **Cacheable**: Mark resources as cacheable or non-cacheable to control reuse of responses.
- **Uniform Interface**: Simplify the architecture by applying general rules for resource interaction.
  - **Resource-Based**: Resources are identified by URIs.
  - **Manipulation of Resources Through Representations**: Clients work with resource representations.
  - **Self-descriptive Messages**: Messages include detailed information for processing.
  - **Hypermedia as the Engine of Application State (HATEOAS)**: Application state is managed through hyperlinks.

## HTTP Methods
- **GET**: Retrieve resource information.
- **POST**: Create a new resource.
- **PUT**: Update an existing resource.
- **DELETE**: Remove a resource.
- **PATCH**: Apply partial updates to a resource.
- **OPTIONS**: Get supported HTTP methods.
- **HEAD**: Get headers for a resource.

## Status Codes
### 2xx Success
- `200 OK`: Success with response data.
- `201 Created`: Resource created.
- `204 No Content`: Success without response data.

### 3xx Redirection
- `301 Moved Permanently`: Resource moved.
- `304 Not Modified`: Resource not modified since last request.

### 4xx Client Error
- `400 Bad Request`: Invalid request.
- `401 Unauthorized`: Authentication required.
- `403 Forbidden`: Request not permitted.
- `404 Not Found`: Resource not found.
- `405 Method Not Allowed`: HTTP method not allowed.

### 5xx Server Error
- `500 Internal Server Error`: Generic server error.
- `503 Service Unavailable`: Server unavailable.

## Best Practices
- Use **nouns** for resource paths (e.g., `/users`).
- Be consistent in naming and format.
- Use **plural** nouns for resources.
- Represent relationships with nested resources (e.g., `/users/123/posts`).
- Use HTTP headers for content type and authentication.
- Include **hypermedia links** in responses to guide clients.
- Apply appropriate HTTP status codes for responses.
- Secure APIs with **HTTPS** and **OAuth/JWT**.

This cheat sheet summarizes key REST principles, methods, status codes, and best practices for designing and interacting with RESTful APIs.
