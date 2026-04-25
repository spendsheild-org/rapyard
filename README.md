## ⚙️ CI/CD Workflow Index

RapYard uses a deterministic, multi‑pipeline CI/CD system.  
Each workflow is isolated, purpose‑built, and mapped to a specific branch.

### Core CI
| File | Purpose |
|------|---------|
| `main.yml` | Lint, typecheck, tests, core CI |

### Mobile App (Expo/EAS)
| File | Purpose |
|------|---------|
| `production.yml` | Production EAS builds (Android + iOS) |
| `canary.yml` | Preview builds for PRs/dev/staging |
| `release.yml` | Semantic versioning + GitHub Releases |
| `expo-preview.yml` | Preview QR builds |
| `expo-submit.yml` | App Store / Play Store submission |
| `expo-ota.yml` | OTA updates via EAS Update |

### Workers
| File | Purpose |
|------|---------|
| `worker-docker.yml` | Build + push Docker worker image |
| `worker-queue.yml` | Restart PM2 worker on deploy |

### Admin Panel
| File | Purpose |
|------|---------|
| `admin-deploy.yml` | Build + deploy admin panel to server |

### Infrastructure
| File | Purpose |
|------|---------|
| `terraform-deploy.yml` | Terraform IaC deploy pipeline |

### Security & Monitoring
| File | Purpose |
|------|---------|
| `sentry-release.yml` | Sentry release automation |
| `security-scan.yml` | Dependency + vulnerability scanning |

### Utilities
| File | Purpose |
|------|---------|
| `monorepo-cache.yml` | Multi‑package dependency caching |
| `notifications.yml` | Slack/Discord notifications |
