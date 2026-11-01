# Provider & Application Architecture

This documentation stage covers the design and execution of federated single sign-on (SSO) delivery paths via Authentik.

## ⚙️ Core Architecture Concepts
* **The Provider:** Defines *how* Authentik communicates with an external app (the technical protocol configuration, certificate validation rules, encryption types, and endpoint URLs).
* **The Application:** Defines *what* the user sees on their dashboard portal (the friendly name, application branding, and access policies tied directly to it).


The core goal of setting up a Provider and an Application in Authentik is to decouple user identities from specific platforms—acting as a centralized gatekeeper that securely translates and passes user authentication data to external tools using modern security standards (like SAML or OIDC).
Here is exactly what the goal is and a detailed log of what was accomplished during that phase:

🎯 The Strategic Goal

* **Centralized Gatekeeping:** Instead of manually provisioning user accounts on every individual lab application, you handle it all in Authentik.
* **Token-Based Handshakes:** To hide sensitive user passwords from external apps, passing secure cryptographic signatures (assertions/tokens) instead.
* **Frictionless Enforcement:** To drop heavy security policies (like multi-factor validation) right onto the login pipeline without modifying the application's underlying code.

---
