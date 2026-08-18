# advanced-jenkins-pipeline
# Experiment : Advanced Jenkins Pipeline and Job Management

## 📌 Overview
This repository contains the setup, configuration script (`Jenkinsfile`), and step-by-step documentation for **Experiment No. 6: Advanced Jenkins Pipeline and Job Management**.

The objective of this practical experiment is to demonstrate advanced CI/CD techniques in Jenkins, including:
* **Parameterized Pipelines** using choice parameters (`DEPLOY_ENV`).
* **Environment Variables** (both custom and built-in Jenkins variables).
* **Conditional Stage Execution** using `when` expressions.
* **Manual Input / Human Approval Steps** for production deployments.
* **Post-Execution Handlers** (`success`, `failure`, `always`).
* **SCM Integration** running Jenkins tasks dynamically from a GitHub repository.

---

## 🚀 Key Concepts & Pipeline Features

| Feature | Implementation | Description |
| :--- | :--- | :--- |
| **Choice Parameter** | `params.DEPLOY_ENV` | Allows selection between `development`, `staging`, and `production` environments prior to build execution. |
| **Environment Block** | `APP_NAME`, `VERSION` | Defines global environment metadata used across stages. |
| **Built-in Variables** | `${BUILD_NUMBER}`, `${JOB_NAME}`, `${WORKSPACE}` | Captures execution context dynamically. |
| **Conditional Stage** | `when { expression { ... } }` | Ensures deployment stages execute only for their intended target environment. |
| **Manual Approval** | `input message: ...` | Pauses pipeline execution at the Production stage until manual sign-off is granted via the Jenkins UI. |
| **Post Actions** | `post { success / failure / always }` | Executes cleanup, logging, or notifications based on the overall build outcome. |

---
