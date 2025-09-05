# Lab 1 - Full-Stack Integration Analysis

## Scenario
Our team is designing a MERN stack application. While the technologies are set, we still need to clarify how the **React frontend** and **Express backend** will interact. The main concerns are **CORS (Cross-Origin Resource Sharing)**, **environment variable management**, and **choosing the right data-fetching strategy**.

---

## Task 2: Written Reflection

### Question 1: CORS Explained  
**What is a CORS error and why does it occur in a MERN stack app? Describe two strategies to fix it during local development.**

A **CORS error** occurs when the browser blocks requests from one origin (like `localhost:3000` for React) to another origin (like `localhost:5000` for Express). This is a browser security measure.  

Two strategies to solve this:  
- **Enable CORS on the server** using the `cors` middleware to allow trusted origins.  
- **Use a proxy in React** so API requests are routed through the development server, avoiding cross-origin issues.  

---

### Question 2: Environment Management  
**Why is hardcoding API URLs a bad practice, and how do environment variables help on both client and server?**

Hardcoding API URLs makes the app less secure and harder to maintain across different environments.  

**Environment variables** solve this by:  
- **Client side**: Using `.env` with `REACT_APP_` variables (e.g., `REACT_APP_API_URL`).  
- **Server side**: Using `.env` with the `dotenv` package to keep sensitive values like database URLs out of the codebase.  

This keeps apps secure, flexible, and consistent.  

---

### Question 3: Data Fetching Trade-offs  
**What is one key advantage of using axios over fetch in a complex app?**

The main advantage of **axios** is **ease of use and built-in features**. It automatically parses JSON, handles errors more cleanly, and supports extras like interceptors, timeouts, and request cancellation. This makes it better for complex applications than the native `fetch` API.  

---

## Summary
- **CORS** protects browsers but requires configuration to allow frontend-backend communication.  
- **Environment variables** prevent hardcoding and make deployments more secure and manageable.  
- **Axios** offers more powerful features than `fetch`, making it a strong choice for complex applications.  

Together, these practices support a **secure and scalable full-stack architecture**.