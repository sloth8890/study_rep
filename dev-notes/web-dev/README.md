# Dive into the Web Development
## Introduction

This section, we will cover knowledges you need for web developments. 

## Ports

Port is a numerical identifier that helps differentiate and direct data traffic to the appropriate service on a machine. It is similar to how wharfs at a harbor are designated locations for ships to dock.

If your Node.js server is running on port 3000, it means the server is stationed at the "wharf" or port 3000. Clients connecting to this server need to specify the port (e.g., http://localhost:3000) to establish communication with the Node.js service.

### Why ports?

Ports enable multiple services to run independently on the same machine without interference. Each service is associated with a unique port, ensuring that incoming data or requests are directed to the correct service.

Here is the common [port numbers](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers)

## HTTP methods
HTTP (Hypertext Transfer Protocol) methods define the actions that can be performed on resources. They are crucial for communication between clients (such as browsers) and servers. Here's a brief overview of commonly used HTTP methods:

GET: Retrieve data from a specified resource.
POST: Submit data to be processed to a specified resource.
PUT: Update a resource or create a new resource if it does not exist.
DELETE: Request the removal of a resource.
PATCH: Apply partial modifications to a resource.
Understanding these methods is essential for building **web applications** and **APIs**.

## Routing

Routing in web development refers to the mechanism of directing users to different pages or resources based on the URL they request. It's a fundamental concept that determines how an application responds to client requests at different endpoints (URLs).

### Basic Concepts

1. **URL Pattern Matching**: Routes match URL patterns to specific handlers or controllers
2. **Parameters**: Routes can include dynamic parameters (e.g., /users/:id)
3. **Query Strings**: Additional data can be passed through query parameters (e.g., ?sort=asc)

### Example Routes

- `/users` - Get all users
- `/users/:id` - Get a specific user by ID
- `/users/:id/posts` - Get all posts for a specific user
- `/posts?sort=asc` - Get all posts sorted by creation date in ascending order


## References
- [Background](https://doozi316.github.io/web/2019/05/15/WEB2/)
- [Web Server vs WAS](https://gmlwjd9405.github.io/2018/10/27/webserver-vs-was.html#google_vignette)
- [DNS](https://aws.amazon.com/route53/what-is-dns/)