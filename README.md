# MemoPing 📒✨

> MemoPing allows you to easily jot down notes! Is note-taking difficult for you? With MemoPing, you can create memos simply and effortlessly!  
> This is a simple web application that allows anyone to manage their notes easily through real-time synchronization.  
> Reason for starting the project: [Read More](https://devpearl.tistory.com/15)

## Current Version

- **v0.0.2**: Server setup and PostgreSQL connection implemented.

## Version Roadmap

| Stage      | Goal                                                                      | Completion Goal |
| ---------- | ------------------------------------------------------------------------- | --------------- |
| **V0.0.2** | Server setup and PostgreSQL connection                                    | `2024-10-25`    |
| **V0.0.5** | EC2 deployment and performance optimization                               | `2024-`         |
| **V0.0.6** | Feature improvements based on user feedback (search, tags, notifications) | `2024-`         |
| **V1.0.1** | User registration and login features with session management              | `2024-`         |
| **V1.0.3** | Real-time synchronization using WebSocket                                 | `2024-`         |
| **V1.0.4** | Implementation of GraphQL server                                          | `2024-`         |

### Development Timeline

### **V0.0.2: Server Setup and PostgreSQL Connection**

> **Goal**: Set up Express server and PostgreSQL database, write API routes, and integrate with the database, including writing test codes with Vitest.

- **Feature Implementation**:
  - Set up Express server and basic route structure.
  - Connect to PostgreSQL and define Prisma schema.
  - Implement CRUD API endpoints (`POST /memos`, `GET /memos`, `DELETE /memos/:id`).
  - Write unit tests for server and database using Vitest.
- **Completion Goal**: `2024-10-25`
- **Development Period**: `2024-10-23 ~ `

---

### **V0.0.5: EC2 Deployment and Performance Optimization**

> **Goal**: Deploy to AWS EC2 instance in a stable production environment with basic memo functionality and user authentication system.

- **Feature Implementation**:
  - Configure EC2 instance and deployment environment.
  - Set up PostgreSQL database and Prisma connection.
  - Stabilize API including basic memo functionality and user authentication.
  - Set up a reverse proxy using Nginx or Apache.
  - Perform basic tests and set up performance monitoring after deployment.
- **Completion Goal**: `2024-`

---

### **V0.0.6: Feature Improvements Based on User Feedback**

> **Goal**: Enhance user experience by implementing memo search functionality, adding hashtags, and notification features based on user feedback.

- **Feature Implementation**:
  - Implement search functionality based on memo content and title (`GET /memos?search=keyword`).
  - Add hashtag feature and related filtering (`GET /memos?tags=tag1,tag2`).
  - Implement real-time notification functionality when creating or updating memos.
  - Write tests and document the improved features.
- **Completion Goal**: `2024-`

---

### **V1.0.1: User Authentication and Session Management**

> **Goal**: Implement a user authentication system, allowing user registration and login to restrict access and manage memos based on users.

- **Feature Implementation**:
  - User registration functionality (`POST /register`).
  - User login functionality (`POST /login`).
  - Manage authentication using JWT or sessions.
  - Protect API so that only authenticated users can create and view memos.
  - Write tests related to authentication using Vitest.
- **Completion Goal**: `2024-`

---

### **V1.0.3: Real-time Data Synchronization Using WebSocket**

> **Goal**: Use WebSocket for real-time data synchronization when users create or modify memos.

- **Feature Implementation**:
  - Set up WebSocket server and handle client communication.
  - Transmit data in real-time via WebSocket during memo CRUD operations.
  - Write tests for real-time data synchronization using Vitest.
- **Completion Goal**: `2024-`

---

### **V1.0.4: Implementation of GraphQL Server**

> **Goal**: Use GraphQL for more flexible data requests and handling, integrating Prisma with GraphQL.

- **Feature Implementation**:
  - Set up GraphQL server and define schema.
  - Write GraphQL resolvers using Prisma.
  - Implement memo CRUD operations using GraphQL.
  - Write tests for GraphQL API using Vitest.
- **Completion Goal**: `2024-`

## API Documentation

### **Endpoints**

- `POST /memos`: Create a new memo.
- `GET /memos`: Retrieve all memos.
- `GET /memos?search=keyword`: Search for memos by keyword.
- `GET /memos?tags=tag1,tag2`: Filter memos by hashtags.
- `DELETE /memos/:id`: Delete a memo by its ID.

## Version Information

For detailed version information, please refer to the [CHANGELOG.md](./CHANGELOG.md).
