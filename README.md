# Neha_Gopinath_CI/CD-Concepts-L1

Problem Statement

The objective of this assignment is to understand and differentiate between Continuous Integration (CI), Continuous Delivery (CD), and Continuous Deployment (CD). The assignment also compares the manual and automated approval processes involved in Continuous Delivery and Continuous Deployment.

Additionally, a theoretical CI/CD pipeline is designed for a simple web application, including the tools that can be used at each stage of the software development lifecycle.

Detailed Description: Differentiate between Continuous Integration, Continuous
Delivery, and Continuous Deployment.

# Difference Between Continuous Integration, Continuous Delivery, and Continuous Deployment

Continuous Integration (CI), Continuous Delivery (CD), and Continuous Deployment are DevOps practices that automate different stages of the software development and release process. Although they are closely related, each has a different purpose.

## Difference Between Continuous Integration, Continuous Delivery, and Continuous Deployment

| Feature | Continuous Integration (CI) | Continuous Delivery (CD) | Continuous Deployment (CD) |
| :--- | :--- | :--- | :--- |
| **Definition** | Frequently integrates code changes into a shared repository and automatically builds and tests the code. | Automatically prepares the application for release after successful builds and tests. | Automatically deploys the application to production after all required checks pass. |
| **Main Goal** | Detect and fix integration issues early. | Keep the application ready for production release at any time. | Deliver new features and fixes to users as quickly as possible. |
| **Build** | Automated | Automated | Automated |
| **Testing** | Automated | Automated | Automated |
| **Staging Deployment** | Optional | Usually automated | Usually automated |
| **Production Deployment** | Manual | Manual after approval | Fully automated |
| **Manual Approval** | Not applicable | Usually required | Not required |
| **Human Intervention** | Required mainly for development and code changes | Required before production release | Minimal; deployment is automated |
| **Release Speed** | Fast integration and feedback | Fast and controlled releases | Fastest release process |
| **Example Tools** | GitHub Actions, Jenkins, GitLab CI | GitHub Actions, Jenkins, GitLab CI | GitHub Actions, Jenkins, GitLab CI/CD |




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

![](data:image/svg+xml;charset=utf-8,%3Csvg%20font-family%3D%22-apple-system-body%2C%20ui-sans-serif%2C%20-apple-system%2C%20system-ui%2C%20%26quot%3BSegoe%20UI%26quot%3B%2C%20Helvetica%2C%20%26quot%3BApple%20Color%20Emoji%26quot%3B%2C%20Arial%2C%20sans-serif%2C%20%26quot%3BSegoe%20UI%20Emoji%26quot%3B%2C%20%26quot%3BSegoe%20UI%20Symbol%26quot%3B%22%20font-weight%3D%22400%22%20data-d-component%3D%22svg%22%20fill%3D%22currentColor%22%20style%3D%22color%3Argb(13%2C%2013%2C%2013)%22%20viewBox%3D%220%200%20320%20520%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%3Crect%20width%3D%22320%22%20height%3D%22520%22%20rx%3D%2228%22%20fill%3D%22%23FFFFFF%22%2F%3E%3Crect%20x%3D%2260%22%20y%3D%2224%22%20width%3D%22200%22%20height%3D%2244%22%20rx%3D%2216%22%20fill%3D%22%232563EB%22%2F%3E%3Ctext%20x%3D%22160%22%20y%3D%2250%22%20text-anchor%3D%22middle%22%20font-family%3D%22Arial%22%20font-size%3D%2216%22%20fill%3D%22white%22%20font-weight%3D%22700%22%3ECode%20Commit%3C%2Ftext%3E%3Ctext%20x%3D%22160%22%20y%3D%2264%22%20text-anchor%3D%22middle%22%20font-family%3D%22Arial%22%20font-size%3D%2211%22%20fill%3D%22%23DBEAFE%22%3EGitHub%20%2F%20Git%3C%2Ftext%3E%3Cpath%20d%3D%22M160%2068%20L160%2084%22%20stroke%3D%22%2394A3B8%22%20stroke-width%3D%222.5%22%20stroke-linecap%3D%22round%22%2F%3E%3Cpolygon%20points%3D%22154%2C84%20166%2C84%20160%2C94%22%20fill%3D%22%2394A3B8%22%2F%3E%3Crect%20x%3D%2252%22%20y%3D%2294%22%20width%3D%22216%22%20height%3D%2252%22%20rx%3D%2218%22%20fill%3D%22%23EEF4FF%22%2F%3E%3Ctext%20x%3D%22160%22%20y%3D%22114%22%20text-anchor%3D%22middle%22%20font-family%3D%22Arial%22%20font-size%3D%2216%22%20fill%3D%22%23111827%22%20font-weight%3D%22700%22%3EContinuous%20Integration%3C%2Ftext%3E%3Ctext%20x%3D%22160%22%20y%3D%22130%22%20text-anchor%3D%22middle%22%20font-family%3D%22Arial%22%20font-size%3D%2212%22%20fill%3D%22%234B5563%22%3EAutomated%20Build%20%2B%20Tests%3C%2Ftext%3E%3Cpath%20d%3D%22M160%20146%20L160%20162%22%20stroke%3D%22%232563EB%22%20stroke-width%3D%222.5%22%20stroke-linecap%3D%22round%22%2F%3E%3Cpolygon%20points%3D%22154%2C162%20166%2C162%20160%2C172%22%20fill%3D%22%232563EB%22%2F%3E%3Crect%20x%3D%2240%22%20y%3D%22172%22%20width%3D%22240%22%20height%3D%22118%22%20rx%3D%2222%22%20fill%3D%22%23F8FAFC%22%20stroke%3D%22%23BFDBFE%22%2F%3E%3Ctext%20x%3D%2256%22%20y%3D%22192%22%20font-family%3D%22Arial%22%20font-size%3D%2215%22%20fill%3D%22%231D4ED8%22%20font-weight%3D%22700%22%3EContinuous%20Delivery%3C%2Ftext%3E%3Crect%20x%3D%2256%22%20y%3D%22202%22%20width%3D%22208%22%20height%3D%2224%22%20rx%3D%2212%22%20fill%3D%22%23DBEAFE%22%2F%3E%3Ctext%20x%3D%22160%22%20y%3D%22218%22%20text-anchor%3D%22middle%22%20font-family%3D%22Arial%22%20font-size%3D%2212%22%20fill%3D%22%231E3A8A%22%3EDeploy%20to%20Staging%3C%2Ftext%3E%3Crect%20x%3D%2256%22%20y%3D%22232%22%20width%3D%22208%22%20height%3D%2224%22%20rx%3D%2212%22%20fill%3D%22%23FDE68A%22%2F%3E%3Ctext%20x%3D%22160%22%20y%3D%22248%22%20text-anchor%3D%22middle%22%20font-family%3D%22Arial%22%20font-size%3D%2212%22%20fill%3D%22%2392400E%22%3EManual%20Approval%3C%2Ftext%3E%3Crect%20x%3D%2256%22%20y%3D%22262%22%20width%3D%22208%22%20height%3D%2218%22%20rx%3D%229%22%20fill%3D%22%23DCFCE7%22%2F%3E%3Ctext%20x%3D%22160%22%20y%3D%22274%22%20text-anchor%3D%22middle%22%20font-family%3D%22Arial%22%20font-size%3D%2211%22%20fill%3D%22%23166534%22%3EReady%20for%20Production%3C%2Ftext%3E%3Cpath%20d%3D%22M160%20290%20L160%20306%22%20stroke%3D%22%230EA5E9%22%20stroke-width%3D%222.5%22%20stroke-linecap%3D%22round%22%2F%3E%3Cpolygon%20points%3D%22154%2C306%20166%2C306%20160%2C316%22%20fill%3D%22%230EA5E9%22%2F%3E%3Crect%20x%3D%2240%22%20y%3D%22316%22%20width%3D%22240%22%20height%3D%22132%22%20rx%3D%2222%22%20fill%3D%22%23F5FFF8%22%20stroke%3D%22%23BBF7D0%22%2F%3E%3Ctext%20x%3D%2256%22%20y%3D%22336%22%20font-family%3D%22Arial%22%20font-size%3D%2215%22%20fill%3D%22%23047857%22%20font-weight%3D%22700%22%3EContinuous%20Deployment%3C%2Ftext%3E%3Crect%20x%3D%2256%22%20y%3D%22348%22%20width%3D%22208%22%20height%3D%2224%22%20rx%3D%2212%22%20fill%3D%22%23D1FAE5%22%2F%3E%3Ctext%20x%3D%22160%22%20y%3D%22364%22%20text-anchor%3D%22middle%22%20font-family%3D%22Arial%22%20font-size%3D%2212%22%20fill%3D%22%23065F46%22%3EBuild%20%2B%20Tests%20Passed%3C%2Ftext%3E%3Crect%20x%3D%2256%22%20y%3D%22378%22%20width%3D%22208%22%20height%3D%2222%22%20rx%3D%2211%22%20fill%3D%22%23A7F3D0%22%2F%3E%3Ctext%20x%3D%22160%22%20y%3D%22393%22%20text-anchor%3D%22middle%22%20font-family%3D%22Arial%22%20font-size%3D%2212%22%20fill%3D%22%23065F46%22%3EAutomatic%20Production%3C%2Ftext%3E%3Crect%20x%3D%2256%22%20y%3D%22406%22%20width%3D%22208%22%20height%3D%2224%22%20rx%3D%2212%22%20fill%3D%22%2310B981%22%2F%3E%3Ctext%20x%3D%22160%22%20y%3D%22422%22%20text-anchor%3D%22middle%22%20font-family%3D%22Arial%22%20font-size%3D%2212%22%20fill%3D%22white%22%3EDeploy%20to%20Users%3C%2Ftext%3E%3Cpath%20d%3D%22M160%20430%20L160%20446%22%20stroke%3D%22%23059669%22%20stroke-width%3D%222.5%22%20stroke-linecap%3D%22round%22%2F%3E%3Cpolygon%20points%3D%22154%2C446%20166%2C446%20160%2C456%22%20fill%3D%22%23059669%22%2F%3E%3Crect%20x%3D%2274%22%20y%3D%22456%22%20width%3D%22172%22%20height%3D%2234%22%20rx%3D%2217%22%20fill%3D%22%23111827%22%2F%3E%3Ctext%20x%3D%22160%22%20y%3D%22477%22%20text-anchor%3D%22middle%22%20font-family%3D%22Arial%22%20font-size%3D%2214%22%20fill%3D%22white%22%20font-weight%3D%22700%22%3ELive%20Application%3C%2Ftext%3E%3C%2Fsvg%3E)

Key difference: Continuous Delivery includes a manual approval step before production, while Continuous Deployment automatically deploys to production after successful testing.