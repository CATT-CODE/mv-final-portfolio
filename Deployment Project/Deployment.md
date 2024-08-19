# Deployment Project: Automated Testing for Data Factory Containers via SonarQube (CI/CD)

[Link to Automated Testing via SonarQube Design Document](https://docs.google.com/document/d/1_DigOxQ-D8hb8iQfmEJAFTum6j2KO4a3gFSQ_ylu4r8/edit?usp=sharing)

## Overview of the Project

This project integrates SonarQube analysis into our Jenkins-based CI/CD pipeline to ensure the quality and reliability of our ELT (Extract, Load, Transform) framework's Docker containers. By automating test coverage and quality analysis, this project aims to improve the development lifecycle of our data factory containers, ensuring they meet high standards of quality from design to deployment.

### Purpose and Users

- **Users:** The primary users are the development and operations teams responsible for maintaining and deploying the ELT framework within our data factory.
- **Job:** The system aims to improve code quality by identifying and addressing code smells, security vulnerabilities, and bugs. It also ensures high test coverage and automates quality assurance within the CI/CD pipeline.
- **Inspiration:** This project was initiated to address the need for a more rigorous and automated quality assurance process within the CI/CD pipeline, ensuring that our data factory containers are both reliable and maintainable.
- **Key Features:** The key features include SonarQube integration for automated code analysis, the implementation of quality gates to enforce code standards, and the streamlined deployment of Docker containers using Jenkins.

### STAR Interview Questions

- **Situation:** Our ELT framework's Docker containers required more rigorous quality checks to ensure reliability. The existing process lacked automated quality assurance, which led to the integration of SonarQube into our Jenkins CI/CD pipeline.
- **Task:** The task involved setting up a CI/CD pipeline that could automatically analyze code quality and test coverage using SonarQube during the build process, ensuring that only code meeting our quality standards would be deployed.
- **Action:** I configured the Jenkins pipeline to include steps for building Docker containers, running unit tests, and performing SonarQube analysis. Quality gates were defined within SonarQube to enforce coding standards, and automated checks were integrated into the pipeline.
- **Result:** The result was a more robust CI/CD pipeline that automatically ensures code quality and reliability before deployment. This integration has reduced the number of bugs and security vulnerabilities in our ELT framework and has streamlined the development process.

### CI/CD Pipeline Flow

<img width="600" alt="image" src="https://github.com/user-attachments/assets/d55ed9f4-c931-43a6-bc19-bac9cd91f91d">

Below is a brief overview of the CI/CD pipeline:

1. **GitHub Repository (Code Commit):** Developers commit code to the GitHub repository.
2. **Manual Trigger in Jenkins:** Developers manually trigger the build process in Jenkins, selecting the appropriate job and specifying their Git branch.
3. **Docker Build & Test:** The Docker container is built, and automated tests are executed. The results determine the next steps in the pipeline.
4. **SonarQube Quality Gate Check:** If the build and tests succeed, SonarQube analyzes the code against predefined Quality Gates.
5. **Decision Points:**
   - **If the code passes the Quality Gate:** The Docker container is pushed to AWS Elastic Container Registry for deployment.
   - **If the code fails:** Developers are notified, and the container is not pushed, preventing deployment of substandard code.

### Technologies Used

- **Jenkins:** For automating the CI/CD pipeline.
- **Docker:** To package the ELT framework into containers.
- **SonarQube:** For analyzing code quality and test coverage.

### Competencies

### JF 1.7: Can follow company, team, or client approaches to continuous integration, version, and source control

- **Situation:** Integrating SonarQube into the CI/CD pipeline required adherence to our company’s standards for continuous integration and source control.
- **Action:** I configured the Jenkins pipeline to ensure that each code commit was automatically tested, analyzed, and versioned according to our company’s guidelines. The integration with SonarQube ensured that quality checks were a mandatory part of this process.
- **Result:** The continuous integration process is now more reliable, with automated checks ensuring that all code meets our quality standards before it is merged and deployed.

### JF 4.6: Can test code and analyze results to correct errors found using unit testing

- **Situation:** The reliability of our ELT framework’s Docker containers depended heavily on thorough testing during the CI/CD process.
- **Action:** I implemented automated unit tests within the Docker containers, ensuring that these tests were executed as part of the Jenkins pipeline. The results were analyzed by SonarQube, which identified any errors or issues in the code.
- **Result:** The automated testing and analysis process has significantly reduced the occurrence of bugs and errors in our deployed containers, leading to a more reliable and maintainable system.

### JF 4.7: Can conduct a range of test types, such as Integration, System, User Acceptance, Non-Functional, Performance, and Security testing

- **Situation:** Ensuring the quality of our ELT framework required multiple types of testing to be integrated into the CI/CD pipeline.
- **Action:** I configured the Jenkins pipeline to run various test types, including unit tests for functionality and SonarQube for static code analysis and security testing. This comprehensive approach ensured that all aspects of the code were evaluated before deployment.
- **Result:** The comprehensive testing process has improved the overall quality and security of our ELT framework, ensuring that only code that meets all required criteria is deployed.
