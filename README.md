# ykube-app

**kr8 is a Kubernetes platform operator that turns a single custom resource into a fully managed developer platform.**

Define capabilities (databases, message queues, and more), deploy applications, and expose a web console — all driven by a `Platform` CR and reconciled by the kr8 operator. Teams get a self-service platform; operators get a single place to manage it.

---

## Quick Install

```sh
kubectl apply -f https://github.com/ykube-app/kr8/releases/latest/download/install.yaml
```

This installs the CRDs and deploys the operator in the `kr8-system` namespace. See the [kr8 README](https://github.com/ykube-app/kr8) for next steps.

---

## Repositories

| Repo | Description |
|------|-------------|
| [kr8](https://github.com/ykube-app/kr8) | Core platform — operator, backend API, and web console |
| [catalog](https://github.com/ykube-app/catalog) | Capability and application definitions available to kr8 platforms |
| [demo-app](https://github.com/ykube-app/demo-app) | Reference application for testing and demonstrating the platform |

---

## Contributing

Start with [kr8](https://github.com/ykube-app/kr8) — it contains the operator (Go), backend API (Go/chi), and web console (React + TypeScript).

```sh
# Run the operator locally
cd operator && make install && make run

# Run the backend + console
cd backend && go run main.go
cd console && npm install && npm run dev

# Run all tests
cd operator && make setup-envtest && make test
cd backend && go test ./...
cd console && npm test -- --run
```

Open an issue before starting large changes. PRs welcome.

---

## License

Copyright 2026. Licensed under the [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0).
