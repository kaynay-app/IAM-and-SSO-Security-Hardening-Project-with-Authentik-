### Phase 3: Cryptographic Environment Isolation
To decouple hardcoded deployment settings from the universal orchestration stack, local folder anchors were formatted on the sda file system. 
* Secure, cryptographic secret strings were generated locally.
* These variables were outputted cleanly into an isolated `.env` environment file.
* A self signed certificate template was generated on the primary CA to allow secure communication between AD and IAM server.
* This ensures no plain-text database credentials or application keys are exposed via the global docker-compose configuration schema.
