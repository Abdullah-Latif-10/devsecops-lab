# DevSecOps Lab

Express task API with automated secret scanning, static analysis, dependency scanning, and container scanning.

## Run locally

```sh
npm ci
npm start
```

The API listens on port 3000. Check `/health` and `/info`; use `/add?a=2&b=3` to add two numbers.

## Security checks

```sh
npm run sast
npm audit --omit=dev --audit-level=high
```

GitHub Actions runs Gitleaks, ESLint security rules, npm audit, Trivy config/image scanning, and creates a CycloneDX SBOM artifact.
