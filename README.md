# 🛠️ Reusable Composite GitHub Actions Suite

[![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-Composite%20Workflows-2088FF?style=flat-square&logo=githubactions&logoColor=white)](https://github.com/jgu7man/actions)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)](LICENSE)

A centralized collection of production-ready, composite **GitHub Actions** and Docker deployment actions designed to standardize CI/CD pipelines across repositories.

---

## 📦 Available Actions

### 1. ⚡ `cache-dependencies`
Intelligently manages Node.js dependencies by hashing `package.json` and `package-lock.json`, restoring cached `node_modules`, and running `npm install` only when dependencies change.

```yaml
- name: Cache & Install Dependencies
  uses: jgu7man/actions/cache-dependencies@main
  with:
    workingDir: "."
    targetBranch: "main"
```

### 2. 🚀 `deploy-firebase-function`
A containerized Docker action that validates, builds, and deploys Firebase Cloud Functions to Google Cloud Platform with secret token management.

```yaml
- name: Deploy Firebase Cloud Function
  uses: jgu7man/actions/deploy-firebase-function@main
  with:
    firebaseToken: ${{ secrets.FIREBASE_TOKEN }}
    projectId: "my-production-project"
```

---

## 📄 License

Distributed under the [MIT License](LICENSE). Created by [Jorge Guzmán (@jgu7man)](https://github.com/jgu7man).
