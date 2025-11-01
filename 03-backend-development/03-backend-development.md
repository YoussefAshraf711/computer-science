[العربي](./03-backend-development_ar.md)

# <a name="-3-backend-development"></a>⚙️ Chapter 3: Backend Development

## 1. What is it?

Backend Development, or "Server-Side Development," is the building and maintenance of the hidden "brain" that powers any application. It's everything that happens behind the scenes that the user doesn't see, from data processing and database communication to managing business logic and security.

If the Frontend is the beautiful storefront and restaurant, the Backend is the kitchen, storage rooms, accounting system, and the manager who runs all the operations.

## 2. What does the specialist do?

A Backend Developer is the engineer who builds and maintains the stability and performance of the server, application, and database. Their tasks include:

* Building Application Programming Interfaces (APIs): Creating organized and secure "Endpoints" that the Frontend (or mobile apps) use to request or send data.
* Managing Business Logic: Writing the code that implements the application's core rules (e.g., how a product's price is calculated, what are the conditions for publishing a new post).
* Interacting with Databases: Designing, creating, and querying databases to store and retrieve information.
* Authentication & Authorization: Verifying the identity of users (Authentication) and determining the permissions granted to them (Authorization).
* Ensuring Security and Performance: Protecting the server from attacks and ensuring it can handle a large number of users (Scalability).

## 3. Sub-domains

* API Development: Specializing in designing and building efficient and secure APIs, whether REST or GraphQL.
* Database Engineering: Focusing on designing complex database structures, optimizing query performance, and ensuring data integrity.
* Cloud Infrastructure Engineering: Focusing on deploying and managing Backend services on cloud platforms like AWS or Azure (a role that overlaps with DevOps and Cloud Engineering).
* Distributed Systems Engineering: Building complex backend systems that run on multiple servers simultaneously to achieve high performance and availability.

## 4. Expanded Key Concepts

* `Server`: A computer (or program) that runs continuously to receive requests from clients (like browsers) and send responses.
* `API (Application Programming Interface)`: The contract or common language agreed upon by the Frontend and Backend for communication.
* `Database`: A system for storing data. It is divided into:
  * `Relational (SQL)`: Data organized in interconnected tables (e.g., PostgreSQL).
  * `Non-Relational (NoSQL)`: More flexible and used for unstructured or large-scale data (e.g., MongoDB).
* `Authentication & Authorization`:
  * `Authentication`: Proving identity (Who are you?).
  * `Authorization`: Determining permissions (What can you do?).
* `Caching`: Using fast memory (like Redis) to store frequently requested data to speed up responses and reduce the load on the database.
* `Asynchronous Tasks`: Handling long-running operations (like sending an email, processing a video) in the background using "Job Queues" like Celery or RabbitMQ, so the user doesn't have to wait.
* `Load Balancing`: Distributing incoming requests across multiple servers to prevent overloading a single server and ensure service continuity.

## 5. Expanded Tools & Technologies

* Languages: Node.js (JavaScript/TypeScript), Python, Java, C#, Go, Ruby, PHP.
* Frameworks: Express (Node.js), Django/Flask (Python), Spring (Java), .NET (C#), Gin (Go), Ruby on Rails.
* Databases: PostgreSQL, MySQL, MongoDB, Redis.
* API Types: REST, GraphQL, gRPC.
* Containerization Tools: Docker, Kubernetes.
* Web Servers: Nginx, Apache.

## 6. In-Depth Workflow

Project: Build the Backend for a "create new post" feature in a blog.

 1. Defining the API Endpoint Specification: The developer defines the "contract" with the Frontend team. The request will be a `POST` to the path `/api/posts`. The Request Body must contain `title` and `content`. The Request Header must contain `Authorization: Bearer <JWT>` to identify the user.
 2. Implementing the Controller: The developer writes the function that receives this request. First, it validates the input (is the title empty?). Second, it verifies the JWT and extracts the `user_id` from it to ensure the user is logged in.
 3. Implementing the Business Logic (Service Layer): The controller might call a "Service" that contains additional logic, such as checking for forbidden words in the content.
 4. Interacting with the Database (Data Layer): The service gives a command to the data layer to create a new record in the `posts` table in the database, linking it to the user's `user_id`. An ORM tool (like Prisma or SQLAlchemy) is often used to facilitate this process.
 5. Sending the Response: If the operation is successful, the server sends a `201 Created` response with the data of the new post. If it fails (e.g., the user is not logged in), it sends an appropriate error response like `401 Unauthorized`.
 6. Writing Tests: The developer writes an Integration Test that sends a real `POST` request to the Endpoint (using a separate test database) and ensures the response is `201` and the data was saved correctly.
 7. Deployment: The new code is placed in a Docker container and deployed to the cloud via a CI/CD pipeline.

## 7. Common Job Roles

* Backend Developer / Engineer: The general role.
* API Developer: Specializes in building APIs.
* Database Engineer / Administrator (DBA): Focuses on designing and maintaining databases.
* Cloud Engineer: Specializes in the cloud infrastructure that the Backend runs on.

## 8. A-Z Glossary

<details>
<summary>Click to expand/collapse the glossary</summary>

| Term | Explanation |
|---|---|
| **`Authentication`** | The process of verifying a user's identity (Who are you?). |
| **`Authorization`** | The process of determining a user's permissions (What can you do?). |
| **`Caching`** | Storing frequently used data in fast memory to speed up access. |
| **`Controller`** | In the MVC pattern, it's the part that receives user requests and directs them. |
| **`CRUD`** | An acronym for the four basic database operations: `Create`, `Read`, `Update`, `Delete`. |
| **`Cookie`** | A small text file that a server stores in the user's browser to remember information about them (like login status). |
| **`Database`** | A data storage system. |
| **`Endpoint`** | A specific URL in an API that responds to a specific request (e.g., `/api/users`). |
| **`Environment Variables`** | Variables (like passwords and API keys) stored outside the code for security. |
| **`gRPC`** | A modern, high-performance API framework from Google, an alternative to REST. |
| **`JWT (JSON Web Token)`** | A secure standard for creating "Access Tokens" to verify user identity between requests. |
| **`Load Balancer`** | Distributes requests across multiple servers to prevent overloading a single server. |
| **`Logging`** | Recording events and errors that occur in the application in log files for later analysis. |
| **`Middleware`** | Code that runs in the middle of a request and response, can be used for authentication or logging requests. |
| **`ORM`** | A technique that allows developers to interact with databases using a programming language (like Python) instead of writing SQL. |
| **`Proxy`** | An intermediary server that stands between a client and a final server, can be used for security or caching. |
| **`Queue (Job Queue)`** | A queue for organizing long-running tasks that operate in the background. |
| **`REST`** | A set of architectural principles for designing scalable and easy-to-understand APIs. |
| **`Rate Limiting`** | Limiting the number of requests a user can send to an API in a certain period to protect against attacks. |
| **`Scalability`** | The ability of a system to handle growth in the number of users or the volume of data. |
| **`Schema`** | A blueprint that describes the structure of a database or the expected data format in an API request. |
| **`Session`** | Information that a server stores about a user's session after they log in. |
| **`WebSocket`** | A protocol that allows for a two-way, persistent connection between a client and a server (used in chat apps, games, etc.). |

</details>

[⬆️ Back to Table of Contents](README.md)

