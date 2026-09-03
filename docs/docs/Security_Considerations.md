# RaceDay Security Considerations
This document outlines the security measures planned for the RaceDay API (Part 1).

## 1. Authentication & Password Storage
- Passwords will **never** be stored in plain text. We will use a strong hashing algorithm (e.g., BCrypt) with a unique salt for every user.
- Session management will be used to maintain the user's authenticated state, storing the `UserID` and `Role` securely on the server side.

## 2. Role-Based Access Control (RBAC)
- Every protected API endpoint will check the user's session role before executing.
- If a Participant attempts to access an Organiser-only endpoint (e.g., `POST /api/events`), the API will immediately return a `403 Forbidden` response.

## 3. Data Validation
- All incoming JSON payloads will be validated server-side to prevent SQL injection and malformed data errors.
