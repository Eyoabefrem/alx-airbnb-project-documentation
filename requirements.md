# 📘 Airbnb Clone – Backend Requirements Specification

This document outlines the **technical and functional requirements** for three core backend features of the Airbnb Clone system.

---

## 🔐 1. User Authentication

### Functional Requirements:
- Users must be able to register, log in, and log out.
- Only authenticated users can perform actions like booking or listing properties.
- Passwords must be stored securely using hashing.

### API Endpoints:

| Method | Endpoint        | Description               |
|--------|------------------|---------------------------|
| POST   | /api/register    | Register a new user       |
| POST   | /api/login       | Authenticate user         |
| POST   | /api/logout      | End session or revoke token |

### Request/Response (Example):
**POST /api/register**
```json
Request:
{
  "email": "user@example.com",
  "password": "securePassword",
  "first_name": "John",
  "last_name": "Doe"
}

Response:
{
  "id": 101,
  "token": "jwt_or_session_id"
}
