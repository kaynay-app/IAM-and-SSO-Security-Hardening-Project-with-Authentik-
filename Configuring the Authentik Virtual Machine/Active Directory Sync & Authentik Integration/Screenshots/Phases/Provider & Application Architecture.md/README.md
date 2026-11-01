# Provider & Application Architecture

This documentation stage covers the design and execution of federated single sign-on (SSO) delivery paths via Authentik.

## ⚙️ Core Architecture Concepts
* **The Provider:** Defines *how* Authentik communicates with an external app (the technical protocol configuration, certificate validation rules, encryption types, and endpoint URLs).
* **The Application:** Defines *what* the user sees on their dashboard portal (the friendly name, application branding, and access policies tied directly to it).

---
