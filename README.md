# Container Notes

Technical reference notes on Docker and container security, covering architecture, networking, image hardening, and operational security for containerized workloads.

## Contents

| File | Description |
|---|---|
| `Basics` | Core container concepts: namespaces, cgroups, images, layers, and the Docker engine |
| `Docker basics` | Docker CLI reference, Dockerfile best practices, compose workflows, and registry usage |

## Core Concepts Covered

### Container Architecture

- Linux namespaces (pid, net, mnt, uts, ipc, user) — isolation primitives
- Control groups (cgroups) — resource limiting and accounting
- Union filesystems (OverlayFS) — image layer management
- Container runtimes: containerd, runc, CRI-O

### Networking

- Bridge, host, overlay, and macvlan network drivers
- DNS resolution inside containers
- Port binding and exposure
- Inter-container communication and network segmentation

### Security Hardening

- Running containers as non-root users
- Read-only root filesystems
- Dropping Linux capabilities (`--cap-drop ALL`)
- Seccomp and AppArmor profile application
- Image scanning for CVEs (Trivy, Grype, Snyk)
- Secrets management — avoiding plaintext in environment variables and layers

### Image Best Practices

- Minimal base images (Alpine, Distroless)
- Multi-stage builds to reduce attack surface
- Layer caching and build optimization
- SBOM generation for supply chain visibility

## Security Use Cases

- Identifying privileged container misconfigurations in cloud environments
- Assessing container escape risk via capability and namespace analysis
- Reviewing Dockerfiles for hardening gaps during security reviews
- Integrating image scanning into CI/CD pipelines

## Author

ASHDEX — Security Researcher & Architect
[ashdex.com](https://ashdex.com)
