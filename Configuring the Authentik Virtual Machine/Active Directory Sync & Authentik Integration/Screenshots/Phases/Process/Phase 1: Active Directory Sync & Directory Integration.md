To manage identities from a central authoritative source, Authentik was integrated directly with the Primary Domain Controller (`KLM-DC02`).

* **Secure Transport Pipeline:** Established encrypted LDAPS pathways over Port 636 mapping to `DC=domain,DC=suffix`.
* **Schema Mapping Remediation:** Resolved a critical synchronization failure where user-oriented schema attributes (such as `givenName`) were incorrectly applied to group objects.
* **Property Alignment:** Aligned attributes cleanly to standard Active Directory group Common Names (`cn`) by assigning explicit mapping parameters:
  * `authentik default LDAP Mapping: DN to User Path`
  * `authentik default LDAP Mapping: Name`
* **Result:** Successfully triggered a global directory parsing sequence, dynamically importing **61 distinct Active Directory users and organizational security groups** into Authentik.

---
