Azure DevOps Learning Project

1. Project Overview

This project demonstrates the practical implementation of Azure DevOps fundamentals, including source code management, project planning, CI/CD automation, automated testing and Docker image building.

The objective was to establish an Azure DevOps environment and integrate Azure Repos, Azure Boards and Azure Pipelines into a basic software development workflow.

2. Azure DevOps Environment

* Organisation: twosomeofficial1
* Project: Azure-Devops-Learning-Project
* Repository: Azure-Devops-Learning-Project
* Version Control: Git
* Pipeline Configuration: Azure Pipelines YAML
* Operating System: Ubuntu
* Programming Language: Python 3.12

3. Repository Structure

The repository contains the following files:

Azure-Devops-Learning-Project/
│
├── .gitignore
├── app.py
├── azure-pipelines.yml
├── buildspec.yml
├── Dockerfile
├── Jenkinsfile
├── README.md
└── test_app.py

Key Files

* app.py – Python application source code.
* test_app.py – Automated unit tests.
* azure-pipelines.yml – Azure Pipelines configuration.
* Dockerfile – Instructions for building the Docker image.
* Jenkinsfile – Jenkins pipeline configuration.
* buildspec.yml – AWS CodeBuild configuration.
* .gitignore – Excludes unnecessary files from Git version control.

4. Azure Repos – Source Code Management

An Azure Git repository was created to host the project source code and configuration files.

The local Git repository was connected to Azure Repos, allowing changes to be tracked and pushed to the remote repository.

Git commands used:

git init
git add .
git commit -m "Initial project setup"
git remote add azure <repository-url>
git push -u azure main

5. Azure Boards – Project Management

Azure Boards was configured to organise and track project activities.

Six work items were created:

1. Set up Azure DevOps Repository
2. Configure Azure CI/CD Pipeline
3. Run Python Unit Test
4. Build and Validate Docker Image
5. Prepare Project Documentation
6. Integrate Azure Boards, Repos and Pipelines

These tasks provided a structured way to organise the project and monitor progress.

6. Azure Pipelines – CI/CD Automation

An Azure Pipelines YAML configuration was created to automate Python validation.

The pipeline uses:

* Ubuntu hosted build agent.
* Python 3.12.
* Python package manager (pip).
* Python unittest framework.

The pipeline installs Python, upgrades pip and runs automated unit tests.

Example pipeline configuration:

trigger:
  - main
pool:
  vmImage: 'ubuntu-latest'
steps:
  - task: UsePythonVersion@0
    inputs:
      versionSpec: '3.12'
    displayName: 'Install Python'
  - script: |
      python -m pip install --upgrade pip
      python -m unittest discover -v
    displayName: 'Run Python unit tests'

7. Docker Image Build and Artifact Publishing

The project also includes a Dockerfile for packaging the Python application into a Docker image.

The Azure pipeline execution included a Docker image build stage and a project artifact publishing stage.

The build and publishing logs confirmed that the tasks completed successfully.

8. Workflow Integration

The project demonstrates how the main Azure DevOps services support the software delivery lifecycle:

* Azure Repos stores and manages source code.
* Azure Boards organises project tasks and tracks progress.
* Azure Pipelines automates build and validation activities.

Together, these services provide visibility and structure throughout the development workflow.

9. Challenges and Lessons Learned

During implementation, I gained practical experience in:

* Creating and configuring an Azure DevOps organisation and project.
* Connecting a local Git repository to Azure Repos.
* Managing Git branches, commits and remote updates.
* Creating and organising work items in Azure Boards.
* Configuring YAML-based Azure Pipelines.
* Running automated Python tests.
* Building Docker images and publishing pipeline artifacts.
* Troubleshooting Git synchronisation and pipeline execution issues.

10. Conclusion

This project provided hands-on experience with Azure DevOps and the integration of source control, project management and CI/CD automation.

It strengthened my understanding of version control, Agile project tracking, automated testing, Docker and continuous integration workflows.