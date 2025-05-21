# AWS Amplify Front-End Deployment Templates

This repository provides standardized configuration templates (`amplify.yml` and `.env`) for deploying front-end applications to **AWS Amplify**. It is intended for use by the front-end team at BDD to ensure consistency, reliability, and best practices across all Amplify deployments.

---

## 📦 What's Included

### 🔧 `amplify.yml`
A CI/CD configuration file for AWS Amplify. This template includes:
- Install, build, and deploy phases
- Caching strategies for faster builds
- Hooks for pre/post deployment commands
- Support for monorepo or multi-app setups (optional)

### 🔐 `.env`
An example environment variable file to manage secrets and configuration at build-time. This file is **not** meant to be committed with real credentials.

---

## 🚀 How to Use

1. **Copy the files** into your project root:

```bash
cp templates/amplify.yml ./amplify.yml
cp templates/.env.example .env
```

2. **Update the `.env` file** with project specific values

3. **Connect your repo to AWS Amplify**, then configure the build settings to use the `amplify.yml`

## Note

1. For **pnpm monorepo**, no `.env` file should be added to the root level. Add the necessary `.env` file to each **package** (within `packages` directory) or **app** (within `apps` directory)

## Resources

1. Configuration & usage of `.env` file in **Vite** projects [=>](https://vite.dev/guide/env-and-mode)