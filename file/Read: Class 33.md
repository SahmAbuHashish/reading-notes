# Reading Questions

### What is the primary purpose of JSON Web Tokens (JWTs) and how do they work in terms of encoding and decoding data?

JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

Although JWTs can be encrypted to also provide secrecy between parties, we will focus on signed tokens. Signed tokens can verify the integrity of the claims contained within it, while encrypted tokens hide those claims from other parties. When tokens are signed using public/private key pairs, the signature also certifies that only the party holding the private key is the one that signed it.

---

### How does JWT Authentication integrate with Django REST Framework to secure API endpoints, and what are the key components involved in this process?

JWT (JSON Web Token) authentication integrates with Django REST Framework (DRF) to secure API endpoints by providing a stateless and token-based authentication mechanism.

1. JWT Tokens: JWT is a compact and self-contained token format that consists of three parts: header, payload, and signature. Tokens are digitally signed to ensure their authenticity. The payload contains claims or information about the user, such as user ID or roles.

2. Authentication Process: The JWT authentication process involves the following steps:
   - User Authentication
   - Token Generation
   - Token Storage
   - Token Transmission
   - Token Verification
   - Access Control

3. DRF Integration: DRF provides integration with JWT authentication through the `djangorestframework_simplejwt` package.

---

### Why is Django’s built-in runserver not suitable for production environments, and what are some alternative server options that should be considered for deploying a Django application?

Django's built-in `runserver` command is not suitable for production environments for several reasons:

1. Performance and Scalability: The `runserver` command is single-threaded and single-process, making it inefficient for handling concurrent requests and high traffic.

2. Security: The `runserver` command is intended for development purposes and lacks essential security features needed in production environments.

3. Stability and Reliability: The `runserver` command is not optimized for long-running processes and may not handle issues like process crashes or automatic restarts in case of failures.

For deploying a Django application in production, it is recommended to consider alternative server options, such as:

- Gunicorn (Green Unicorn): Gunicorn is a widely used production-ready server for Django applications. It supports multiple worker processes, making it suitable for handling concurrent requests and improving performance.



