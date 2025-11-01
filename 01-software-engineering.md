[العربي](./01-software-engineering_ar.md)

# <a name="-1-software-engineering"></a>🏗️ Chapter 1: Software Engineering

## 1. What is it?

Software Engineering is the systematic engineering approach to software development. It is not just "writing code," but a complete discipline that applies scientific and engineering principles to the process of designing, developing, testing, deploying, and maintaining complex software and systems.

The fundamental difference between "Programming" and "Software Engineering":

* Programming: Can be an individual activity to solve a specific problem.
* Software Engineering: Is an organized team effort to build a large-scale system that is maintainable and scalable over the long term, ensuring quality, security, and performance.

## 2. What does the specialist do?

A Software Engineer is the "architect" and "builder" in the digital world. Their tasks go beyond writing code to include:

* Translating business needs: Converting user or management requirements into clear technical specifications.
* Making architectural decisions: Designing the overall System Architecture and choosing the appropriate technologies.
* Writing clean and reliable code: Producing code that not only "works" but is also easy to read, maintain, and test by others.
* Ensuring quality: Writing Automated Tests to ensure the program is free of Bugs.
* Collaborating within a team: Using systems like Git to work with a team of developers on the same project.
* Problem-solving: Analyzing complex problems and breaking them down into smaller, solvable parts.
* Product ownership: Feeling a sense of responsibility for the product from its initial idea to its delivery to the user and subsequent maintenance.

## 3. Sub-domains

Software Engineering is not a single field, but branches into many specializations:

* Frontend Development: Building the part that the user interacts with directly in the browser (User Interface - UI).
* Backend Development: Building the "brain" of the application that runs on the server (logic, databases, APIs).
* Full-Stack Development: Working on both the frontend and backend.
* Mobile Development: Building applications that run on iOS and Android systems.
* Game Development: Building video games, which requires skills in Graphics and physics.
* Embedded Systems Engineering: Programming smart devices with limited resources (like home appliances, cars, microcontrollers).
* QA / Test Engineering: Specializing in building advanced automated testing systems to ensure product quality.

## 4. Expanded Key Concepts

* Software Development Life Cycle (SDLC) Models:
  * `Waterfall`: A traditional, rigid model where each phase must be completed before the next begins (planning → design → implementation → testing → deployment). Not suitable for modern projects.
  * `Agile`: A modern philosophy that focuses on Iterative development, delivering small parts of the product quickly, and adapting to change.
  * `Scrum` & `Kanban`: The most famous frameworks for implementing Agile. Scrum is based on short work cycles (Sprints), while Kanban focuses on a continuous workflow.

* Architectural Patterns:
  * `Monolith`: Building the application as a single, integrated unit. Easy at the start but difficult to maintain and scale.
  * `Microservices`: Dividing the application into a set of small, independent services that communicate with each other. Easier to develop, scale, and maintain.
  * `Client-Server`: The basic model for the web, where the client (browser) requests a service from the server.
  * `MVC (Model-View-Controller)`: A common pattern for separating the presentation logic (View) from the data logic (Model) and control logic (Controller).

* Design Principles:
  * `SOLID`: Five fundamental principles in Object-Oriented Programming (OOP) to make code flexible and maintainable.
  * `DRY (Don't Repeat Yourself)`: Don't repeat the same code. Put it in a Function and call it.
  * `KISS (Keep It Simple, Stupid)`: Make the solution as simple as possible. Don't complicate things unnecessarily.

* Programming Paradigms:
  * `Object-Oriented (OOP)`: Organizing code around "Objects" that contain data and behavior.
  * `Functional (FP)`: Organizing code around pure "Functions" that avoid changing state.
  * `Procedural`: Organizing code as a series of commands and steps.

## 5. Expanded Tools & Technologies

* Programming Languages:
  * Java, C#: Powerful for large enterprise backend applications.
  * Python: Excellent for backend applications, data science, and automation.
  * JavaScript / TypeScript: The primary language for the web (Frontend & Backend).
  * Go, Rust: Modern languages focused on high performance and concurrent systems.
  * Kotlin, Swift: The primary languages for mobile development (Android & iOS).
* Frameworks:
  * Backend: Spring (Java), Django/Flask (Python), Node.js/Express (JS), .NET (C#).
  * Frontend: React, Angular, Vue.js.
* Databases:
  * SQL: PostgreSQL, MySQL, SQL Server.
  * NoSQL: MongoDB, Redis, Cassandra.
* Version Control: Git (the tool), GitHub, GitLab, Bitbucket (the platforms).
* Project Management: Jira, Trello, Asana.

## 6. In-Depth Workflow

Project: Add a "Login with Google" feature to a website.
Team: Frontend engineer, backend engineer, product manager.
Methodology: Scrum (two-week sprints).

 1. Sprint Planning Meeting:
     * User Story: "As a new user, I want to log in with my Google account so I can access the application quickly and easily."
     * Task Breakdown:
         * Frontend Task: Design and add a "Login with Google" button. On click, redirect the user to Google's consent screen (OAuth 2.0). After consent, receive an "Authorization Code" from Google.
         * Backend Task: Build a new Endpoint, e.g., /api/auth/google/callback. This endpoint receives the "Authorization Code" from the Frontend, then communicates with Google's servers to exchange it for an "Access Token" and user information (name, email). It then searches the database for the user. If not found, it creates a new account. Finally, it creates a secure "Session Token" (like JWT) and sends it to the Frontend to log the user in.
         * Database Task: Modify the `users` table to add a new `google_id` field.

 2. Development:
     * Each engineer works on their task in a separate Git branch.
     * The Backend engineer might use a tool like Postman to test the endpoint they built independently.

 3. Testing:
     * Unit Tests: The Backend engineer writes a test to ensure the "create new user" function works correctly.
     * Integration Tests: A test is written to ensure the Frontend can send the code to the Backend and receive a JWT successfully.
     * End-to-End (E2E) Tests: Using a tool like Cypress, an automated test is written that simulates a real user clicking the button, logging in via Google, and returning to the site logged in.

 4. Code Review:
     * When tasks are complete, a Pull Request (PR) is created on GitHub.
     * Another engineer reviews the code. They might leave a comment like: "You need to handle the error case if the user denies permission on the Google screen."

 5. Merge & Deploy:
     * After approval, the code is merged into the main branch.
     * Here, the DevOps role begins: The CI/CD system runs automatically, performs all tests, and if they pass, deploys the new version to the servers.

## 7. Common Job Roles

* Frontend Engineer: Focuses on the user experience in the browser.
* Backend Engineer: Focuses on server logic and databases.
* Full-Stack Engineer: Works on both Frontend and Backend.
* Mobile Engineer (iOS/Android): Specializes in mobile applications.
* Software Architect: An expert engineer who designs the overall architecture of complex systems.
* QA Engineer: Writes code to test the code written by other developers.

## 8. A-Z Glossary

<details>
<summary>Click to expand/collapse the glossary</summary>

| Term | Explanation |
|---|---|
| **`Abstract Class`** | A class that cannot be instantiated directly, used as a template for other classes. |
| **`Agile`** | A development philosophy that focuses on rapid iteration and adapting to change. |
| **`API`** | An interface that allows different systems to communicate and exchange data. |
| **`Architecture`** | The overall structure of a system and how its components interact. |
| **`Backend`** | The part of the application that runs on the server and handles data and logic. |
| **`Branch`** | A copy of the code in a `Git` system to work on a new feature in isolation from the original code. |
| **`Bug`** | An error or unexpected behavior in a program. |
| **`Build`** | The process of converting source code into a runnable program. |
| **`Class`** | A template for creating "Objects" in Object-Oriented Programming. |
| **`Code Review`** | The process of reviewing code by other team members to ensure its quality. |
| **`Compiler`** | A program that converts code from a high-level programming language (like C++) to machine language. |
| **`CI/CD`** | Continuous Integration and Continuous Deployment, the process of automating software building, testing, and deployment. |
| **`Database`** | A system for storing and retrieving data in an organized manner. |
| **`Debugging`** | The process of finding and fixing bugs. |
| **`Dependency`** | A library or another program that your project relies on to work. |
| **`Deployment`** | The process of deploying the application to servers to make it available to users. |
| **`Design Pattern`** | A standard, tested solution to a recurring design problem in software engineering. |
| **`Framework`** | A framework that provides a ready-made structure and tools to speed up the development process. |
| **`Frontend`** | The part of the application that the user sees and interacts with in the browser. |
| **`Git`** | The most popular version control system in the world. |
| **`Inheritance`** | A concept in OOP where a class inherits properties and behaviors from another class. |
| **`Interpreter`** | A program that reads and executes code line by line (like Python). |
| **`Library`** | A collection of pre-written code that you can use in your project. |
| **`Merge`** | The process of merging changes from one `branch` to another in `Git`. |
| **`Microservices`** | An architectural pattern that divides an application into small, independent services. |
| **`Monolith`** | An architectural pattern where the application is a single, integrated unit. |
| **`MVC`** | An architectural pattern that separates data (Model), presentation (View), and control (Controller). |
| **`OOP`** | Object-Oriented Programming, a programming paradigm based on objects and classes. |
| **`Polymorphism`** | A concept in OOP meaning "many forms," where an object can take on different forms. |
| **`Pull Request`** | A request to review and merge code from one `branch` to another on platforms like GitHub. |
| **`Refactoring`** | Restructuring and improving code internally without changing its external behavior. |
| **`Repository`** | A repository for storing code and the project (often managed with `Git`). |
| **`REST`** | A set of principles for designing APIs in an organized and easy-to-understand way. |
| **`Scalability`** | The ability of a system to handle an increasing number of users or data. |
| **`SDK`** | Software Development Kit, a set of tools for developing software for a specific platform. |
| **`SOLID`** | Five basic design principles in OOP. |
| **`Sprint`** | A short work cycle (two weeks to a month) in the `Scrum` methodology. |
| **`SQL`** | Structured Query Language, used to communicate with relational databases. |
| **`Testing`** | The process of verifying that a program works as expected and is free of errors. |
| **`UI/UX`** | User Interface (UI) and User Experience (UX). |
| **`Version Control`** | A system for tracking and managing changes in code over time. |

</details>

[⬆️ Back to Table of Contents](README.md)

