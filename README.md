# Neha_Gopinath_CI/CD-Concepts-L1

Problem Statement

The objective of this assignment is to understand and differentiate between Continuous Integration (CI), Continuous Delivery (CD), and Continuous Deployment (CD). The assignment also compares the manual and automated approval processes involved in Continuous Delivery and Continuous Deployment.

Additionally, a theoretical CI/CD pipeline is designed for a simple web application, including the tools that can be used at each stage of the software development lifecycle.

Detailed Description: Differentiate between Continuous Integration, Continuous
Delivery, and Continuous Deployment.

# Difference Between Continuous Integration, Continuous Delivery, and Continuous Deployment

Continuous Integration (CI), Continuous Delivery (CD), and Continuous Deployment are DevOps practices that automate different stages of the software development and release process. Although they are closely related, each has a different purpose.


| Feature                   | Continuous Integration (CI)                                                                              | Continuous Delivery (CD)                                                              | Continuous Deployment (CD)                                                          |
| ------------------------- | -------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| **Definition**            | Frequently integrates code changes into a shared repository and automatically builds and tests the code. | Automatically prepares the application for release after successful builds and tests. | Automatically deploys the application to production after all required checks pass. |
| **Main Goal**             | Detect and fix integration issues early.                                                                 | Keep the application ready for production release at any time.                        | Deliver new features and fixes to users as quickly as possible.                     |
| **Build**                 | Automated                                                                                                | Automated                                                                             | Automated                                                                           |
| **Testing**               | Automated                                                                                                | Automated                                                                             | Automated                                                                           |
| **Staging Deployment**    | Optional                                                                                                 | Usually automated                                                                     | Usually automated                                                                   |
| **Production Deployment** | Manual                                                                                                   | Manual after approval                                                                 | Fully automated                                                                     |
| **Manual Approval**       | Not applicable                                                                                           | Usually required                                                                      | Not required                                                                        |
| **Human Intervention**    | Required mainly for development and code changes                                                         | Required before production release                                                    | Minimal; deployment is automated                                                    |
| **Release Speed**         | Fast integration and feedback                                                                            | Fast and controlled releases                                                          | Fastest release process                                                             |
| **Example Tools**         | GitHub Actions, Jenkins, GitLab CI                                                                       | GitHub Actions, Jenkins, GitLab CI                                                    | GitHub Actions, Jenkins, GitLab CI/CD                                               |




## 1. Continuous Integration (CI)

Continuous Integration is the practice of frequently merging code changes into a shared repository. Every time a developer pushes code, an automated process builds the application and runs tests to identify errors early.

Key features:

- Developers merge code frequently.
- Builds and tests run automatically.
- Helps detect bugs and integration issues early.
- Improves code quality and team collaboration.

Example workflow:

1. Developer writes code.
2. Code is pushed to GitHub.
3. CI tool (such as GitHub Actions or Jenkins) automatically builds the project.
4. Automated tests are executed.
5. Developers receive immediate feedback.



## 2. Continuous Delivery (CD)

Continuous Delivery builds on Continuous Integration by ensuring the application is always ready for release. After the build and testing stages, the application is automatically deployed to a staging environment. However, production deployment requires manual approval.

Key features:

- Automatically builds, tests, and prepares the application.
- Deploys to staging automatically.
- Production release happens only after manual approval.
- Reduces the risk of production releases.

Example workflow:

1. Code is built and tested automatically.
2. Application is deployed to staging.
3. A manager or DevOps engineer reviews the release.
4. After approval, the application is deployed to production.



## 3. Continuous Deployment

Continuous Deployment is the most automated approach. Once the application successfully passes all automated builds, tests, and quality checks, it is automatically deployed to production without any human intervention.

Key features:

- Fully automated release process.
- No manual approval required.
- Faster delivery of new features and bug fixes.
- Requires reliable automated testing.

Example workflow:

1. Developer pushes code.
2. Build and tests run automatically.
3. Quality and security checks are completed.
4. The application is automatically deployed to production.



## Summary

- Continuous Integration (CI): Automatically builds and tests code whenever developers make changes.
- Continuous Delivery (CD): Automatically prepares the application for release, but production deployment requires manual approval.
- Continuous Deployment: Automatically deploys the application to production after all automated checks pass, with no manual approval required.



### Simple Flow Diagram

![](https://www.netsolutions.com/wp-content/uploads/2022/07/ci-and-cd-1024x1019-1.webp)

Key difference: Continuous Delivery includes a manual approval step before production, while Continuous Deployment automatically deploys to production after successful testing.

## Manual vs. Automated Approval: Continuous Delivery vs. Continuous Deployment

The main difference between Continuous Delivery and Continuous Deployment is the approval process before deploying the application to production.


| Feature               | Continuous Delivery                                                      | Continuous Deployment                                      |
| --------------------- | ------------------------------------------------------------------------ | ---------------------------------------------------------- |
| Build and Testing     | Automated                                                                | Automated                                                  |
| Staging Deployment    | Automated                                                                | Automated                                                  |
| Approval              | Manual approval is required before production deployment.                | No manual approval is required.                            |
| Production Deployment | Performed after a person approves the release.                           | Automatically performed after all tests and checks pass.   |
| Human Intervention    | Required before production deployment.                                   | Not required for each release.                             |
| Release Process       | Automated up to the production-ready stage, followed by manual approval. | Fully automated from code commit to production deployment. |




### Continuous Delivery

In Continuous Delivery, the application is automatically built, tested, and deployed to a staging environment. Before it is deployed to production, a developer, manager, or release team manually reviews and approves the release.

**Flow:**

Code → Build → Test → Staging → **Manual Approval** → Production

### Continuous Deployment

In Continuous Deployment, the application is automatically built, tested, and deployed to production when all required checks pass. There is no manual approval step for each release.

**Flow:**

Code → Build → Test → Staging → **Automated Approval/Checks** → Production

### Key Difference

**Continuous Delivery = Manual approval before production**

**Continuous Deployment = Automatic production deployment after successful checks**

## Hands-on Task: Map out a theoretical CI/CD pipeline for a simple web application, listing the tools you might use at each step.

### Pipeline Flow

Developer
    ↓
Source Control
    ↓
Build
    ↓
Test
    ↓
Code Quality Check
    ↓
Deploy to Staging
    ↓
Manual Approval
    ↓
Deploy to Production

| Step                    | Activity                                        | Tools                   |
| ----------------------- | ----------------------------------------------- | ----------------------- |
| 1. Source Control       | Store and manage application code               | GitHub / GitLab         |
| 2. Build                | Build the application and create a container    | Jenkins, Docker         |
| 3. Test                 | Check whether the application works correctly   | Jest, Cypress           |
| 4. Code Quality         | Check code quality and security                 | ESLint, SonarQube, Snyk |
| 5. Deploy to Staging    | Deploy the application to a testing environment | Terraform, Ansible      |
| 6. Manual Approval      | Review the application before production        | Manual Approval         |
| 7. Deploy to Production | Make the application available to users         | AWS / GCP               |

Simple Explanation

Source Control: The developer writes the application code and pushes it to GitHub or GitLab.
Build: Jenkins builds the application, and Docker creates a container for it.
Test: Tools such as Jest and Cypress automatically test the application.
Code Quality: ESLint, SonarQube, and Snyk check the code for quality and security issues.
Staging: Terraform and Ansible are used to deploy the application to a staging environment for further testing.
Manual Approval: A team member reviews the application and approves it for production.
Production: The application is deployed to AWS or GCP, where users can access it.

GitHub / GitLab
      ↓
Jenkins + Docker
      ↓
Jest + Cypress
      ↓
ESLint + SonarQube + Snyk
      ↓
Terraform + Ansible
      ↓
Staging
      ↓
Manual Approval
      ↓
AWS / GCP
      ↓
Production