# 0x02. Session Authentication

## Background Context

In this project, you will implement a Session Authentication system from scratch. You are not allowed to install any external modules.

In the industry, it's common practice to use pre-built modules or frameworks to handle Session Authentication, such as `Flask-HTTPAuth` in Python-Flask. However, for the purpose of learning, we will build each component of this mechanism to gain a deeper understanding of how it works.

## Learning Objectives

1. **What authentication means**
2. **What session authentication means**
3. **What Cookies are**
4. **How to send Cookies**
5. **How to parse Cookies**

## General Overview

### What Authentication Means

**Authentication** is the process of verifying the identity of a user or system. It ensures that someone or something is who or what it claims to be. Common methods include:

- Password-based authentication
- Multi-factor authentication (MFA)
- Biometric authentication
- Token-based authentication

### What Session Authentication Means

**Session authentication** is a method used to maintain a user's authentication status across multiple requests during a session. Key points include:

- Creation of a unique session ID upon user login
- Storage of session data on the server
- Tracking the session ID through client-side cookies
- Maintaining the session until the user logs out or the session times out

### What Cookies Are

**Cookies** are small pieces of data stored on the client side and sent to the server with each request. They are used for:

- Session management
- Personalization
- Tracking user behavior

Types of cookies:

- Session cookies: Temporary, deleted when the browser closes
- Persistent cookies: Remain on the device until they expire or are deleted
- Secure cookies: Only sent over HTTPS
- HttpOnly cookies: Not accessible via JavaScript

### How to Send Cookies

Cookies are sent from the server to the client using the `Set-Cookie` HTTP header. Example:

```http
HTTP/1.1 200 OK
Set-Cookie: sessionId=abc123; Path=/; HttpOnly; Secure; SameSite=Strict
```
