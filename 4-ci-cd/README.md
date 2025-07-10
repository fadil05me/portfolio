# CI/CD Pipelines: Jenkins & GitLab CI

This folder presents the complete CI/CD setups I built during my DevOps bootcamp:

1. **Jenkins pipelines** for automated build, test, and deployment
   Detailed in `cicd.md` (link below)
2. **GitLab CI pipeline** for a previous project
   Preview available via a public `.gitlab-ci.yml`

---

## 1. Jenkins Pipeline (Production → Staging)

Managed via Jenkins with the following stages:

- Clone the repo
- Build Docker image
- Run automated tests
- Push image to private Docker registry
- SSH into target server (Biznet)
- Pull and redeploy containers

Artifacts and UI details documented in:

[`cicd.md`](https://github.com/fadil05me/devops20-dumbways-AhmadFadillah/blob/main/stage2/final-task/cicd.md)

---

## 2. GitLab CI Pipeline

I also worked with GitLab CI to configure a pipeline for my bootcamp project:

- Repository: `wayshub-frontend`
- Configuration: `.gitlab-ci.yml`

Review the full config here:
[GitLab pipeline file](https://gitlab.com/team-2-dumbways/wayshub-frontend/-/blob/main/.gitlab-ci.yml)

More Details: [HERE](https://github.com/fadil05me/devops20-dumbways-AhmadFadillah/blob/main/stage2/week2/day3/README.md)

---

## Summary

- **Jenkins**: Multi-branch pipelines using webhook triggers
- **GitLab CI**: YAML-based job configuration with stages for build/test/deploy
- **Docker integration**: Image creation, registry interaction, and container deployment
- **Deployment automation**: Secure SSH access and scripted redeployment
- **Environment separation**: Dedicated pipelines for production and staging
