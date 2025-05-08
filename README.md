# **ReactJS-Spring-Boot-Full-Stack-App**
<hr>

This project consists of two applications:

- A Spring Boot REST API (`spring-backend`)
- A ReactJS frontend (`react-frontend`)

It is a service-oriented platform focused on establishing and maintaining connections between consumers and small businesses in the **Arts, Entertainment, and Recreation** sector.

## **Applications**
<hr>

### 🔹 `spring-backend`

A Spring Boot Java backend that exposes a REST API to manage hobbies. Its secured endpoints require a valid JWT (access token).

- Stores data in a **MySQL** database.
- Requires JWT for access to protected endpoints.
- Includes Swagger documentation for API testing.

---

### 🔹 `react-frontend`

A ReactJS frontend where:

- **Users** can find and save hobbies.
- **Businesses** can manage their offers.

Login is required via username/password. Upon successful login, a JWT token is used for secured backend API requests.

> Uses **Semantic UI React** for styling.

---

## **Prerequisites**
<hr>

- Java 11+
- npm
- JWT

---

## **Setup Instructions**
<hr>

### 🚀 Clone the Repository

```bash
git clone https://github.com/dharanitharan27/Full-Stack-Project.git
cd Full-Stack-Project
```

---

### ⚛️ Frontend Setup

1. Install Node.js v16.13.1 and npm v8.3.0  
2. Navigate to the frontend folder:

```bash
cd react-frontend
```

3. Install dependencies:

```bash
npm install
```

4. Start the application:

```bash
npm start
```

Access the app at: [http://localhost:4200](http://localhost:4200)

---

### ☕ Backend Setup

1. Install:
   - JDK 11.0.11
   - Docker v20.10.7
   - Docker Compose v1.8.0

2. Navigate to the backend folder:

```bash
cd spring-backend
```

3. Start the backend using Docker:

```bash
docker-compose up --build
```

Backend runs at: [http://localhost:8080](http://localhost:8080)

---

## **API Documentation**
<hr>

Explore API via Swagger:

📍 [http://localhost:8080/swagger-ui/index.html](http://localhost:8080/swagger-ui/index.html)  
💎 OpenAPI docs available at `/v3/api-docs`

### 🔐 Authentication Endpoints

- `/signup` — Register as a **client user**
- `/register` — Register as a **business user**
- `/authenticate` — Obtain a JWT token

Once authenticated, click the 🔒 "Authorize" button in Swagger UI and paste your JWT token to access secured endpoints.

---

## **Email Configuration (Spring Mail)**
<hr>

To enable email confirmation features (like notifications):

1. Specify valid credentials in `application.properties`:

```properties
spring.mail.username=your_email@example.com
spring.mail.password=your_email_password
```

> ⚠️ Without email configuration, calling `/notification` will result in `javax.mail.AuthenticationFailedException`. Other features will continue to work normally.
