Automated CI Pipeline for a Web Application using Jenkins
Project Overview
This project demonstrates how to design and implement a Continuous Integration (CI) pipeline using Jenkins for a modern web application.
The pipeline automatically triggers whenever new code is pushed to the GitHub repository. It performs a series of automated steps — code checkout, dependency installation, testing, building, and artifact packaging — ensuring that the application is always ready for deployment.
The focus is on automation, reliability, and repeatability, which are key principles of modern DevOps practices.
 Objectives
Install and configure Jenkins for CI pipelines.
Automate build and test processes for a web application.
Integrate GitHub with Jenkins for automatic build triggers.
Generate and archive build artifacts.
Understand Jenkins pipeline concepts and job configuration.
 Tech Stack
Language / Framework: Node.js (Express)
Version Control: GitHub
CI Tool: Jenkins
Testing Framework: Jest
Build Tool: npm
 Jenkins Pipeline Overview
Stage	Description
1. Code Checkout	Jenkins pulls the latest code from GitHub (main branch).
2. Dependency Installation	Installs all required dependencies from package.json.
3. Static Code Analysis (Optional)	Runs tools like ESLint for code quality checks.
4. Unit Testing	Executes Jest test cases and generates reports.
5. Build & Package	Packages the web app into a .zip artifact.
6. Post-Build Actions	Archives the build and sends notifications if configured.
 Setup Instructions
1. Install Jenkins
Download and install Jenkins (https://www.jenkins.io/download/)
Start the Jenkins service:
Access Jenkins in your browser at: http://localhost:8080
2. Connect Jenkins to GitHub
Create a new Jenkins job (Pipeline type).
Configure your GitHub repository under Source Code Management.
Add GitHub credentials (username/token).
Optionally, configure a webhook in GitHub for automatic triggers.
3. Create Pipeline Using Jenkinsfile
Add a Jenkinsfile to your repository defining the CI stages.
In Jenkins, set Pipeline Script from SCM and point to your repo’s Jenkinsfile.
4. Trigger and View Builds
Push code changes to the main branch — Jenkins will auto-trigger the pipeline.
Monitor progress in the Jenkins Dashboard → Pipeline Stage View.
