# laniakea-infra

A repository containing all the required infrastructure stack, easily installable with Docker Compose, to support the **Laniakea** ecosystem. 

This orchestrates the core data, caching, security, and routing services needed for development and production deployments.

##  What's Inside (the stack):

This infrastructure stack coordinates the following core services within a single, isolated Docker network:

*   **Database Layer (PostgreSQL):** The primary relational database for persistent data storage. 
*   **Cache & Queue Layer (Redis):** High-performance in-memory data store used for fast caching and managing background job queues.
*   **Secret Management (HashiCorp Vault):** A secure storage system for tightly controlling access to tokens, passwords, certificates, and encryption keys, featuring an accessible Web UI.
*   **Reverse Proxy & SSL (Caddy):** The entry point to the infrastructure. It automatically handles TLS/SSL certificates and handles routing/reverse-proxying external traffic to internal services cleanly.
