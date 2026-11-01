To prove the architecture worked seamlessly, a validation test was done using a dedicated Active Directory test user (`testuser1`) with least privillege principle applied:

1. **The Intercept:** The user attempted to access the application workspace. Authentik successfully intercepted the unauthenticated session.
2. **The Enforcement:** Because of the policy stage attached, the user was prompted for cryptographic device enrollment and verified their second factor.
3. **The Federation:** Upon verification, Authentik signed the authentication payload and executed a flawless single sign-on handoff, granting the user entry into their secure dashboard portal.
4. **The Token Revocation:** To mitigate session hijacking vectors, explicit inactivity limits were configured. After a few minutes of detected user inactivity, the application tokens are automatically revoked and expired. Any subsequent access attempts force a fresh authentication challenge, ensuring tokens cannot be re-used by an external malicious actor.
