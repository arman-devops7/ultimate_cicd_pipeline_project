# BoardgameListingWebApp

## Description

**Board Game Database Full-Stack Web Application.**  
This web application displays lists of board games and their reviews. While anyone can view the board game lists and reviews, they are required to log in to add/edit the board games and their reviews. The 'users' have the authority to add board games to the list and add reviews, and the 'managers' have the authority to edit/delete the reviews on top of the authorities of users.

## Technologies

- **Java**
- **Spring Boot**
- **Amazon Web Services (AWS) EC2**
- **Thymeleaf**
- **Thymeleaf Fragments**
- **HTML5**
- **CSS**
- **JavaScript**
- **Spring MVC**
- **JDBC**
- **H2 Database Engine (In-memory)**
- **JUnit test framework**
- **Spring Security**
- **Twitter Bootstrap**
- **Maven**

## Features

- Full-Stack Application
- UI components created with Thymeleaf and styled with Twitter Bootstrap
- **Authentication and Authorization** using Spring Security:
  - Authentication via username and password.
  - Authorization by granting permissions based on roles:
    - Non-members: Can only view board game lists and reviews.
    - Users: Can add board games and write reviews.
    - Managers: Can edit and delete reviews, in addition to user privileges.
- Deployed on **AWS EC2**
- **JUnit** test framework for unit testing
- **Spring MVC** for a structured application with segregated views, controllers, and database packages
- **JDBC** for database connectivity and interaction
- CRUD operations for managing data in the database
- Schema.sql file for customized schema and initial data input
- Thymeleaf Fragments to reduce redundancy in HTML elements (head, footer, navigation)

---

## CI/CD Pipeline

This application is supported by an **ultimate CI/CD pipeline** designed to ensure efficient deployment, testing, and monitoring. Below are the key components and tools integrated into the pipeline:

### Tools and Technologies:

- **Jenkins**: Used for continuous integration and deployment.
- **Maven**: For project build and dependency management.
- **SonarQube**: For static code analysis and quality assurance.
- **Nexus Repository**: For storing and managing build artifacts.
- **Cloudflare**: For DNS management and security.
- **Prometheus Blackbox Exporter**: For endpoint monitoring and alerting.
- **AWS EC2**: For hosting and deploying the application.

### CI/CD Workflow:

1. **Source Code Management**:
   - Jenkins is configured to pull the latest changes from the Git repository whenever changes are pushed.

2. **Build**:
   - Maven is used to compile the code, resolve dependencies, and package the application.
   - Runs unit tests as part of the build process to ensure code stability.

3. **Code Quality**:
   - SonarQube scans the code for bugs, vulnerabilities, and code smells, ensuring adherence to quality standards.
   - Jenkins integrates with SonarQube to generate detailed reports for developers.

4. **Artifact Management**:
   - The build artifacts (e.g., JAR/WAR files) are published to Nexus Repository for version control and future deployment.

5. **Deployment**:
   - Jenkins deploys the application to AWS EC2 instances.
   - Environment-specific configurations (e.g., production, staging) are managed via environment variables.

6. **DNS Management**:
   - Cloudflare handles DNS routing, caching, and security for the application.

7. **Monitoring and Alerting**:
   - Prometheus Blackbox Exporter monitors the health of endpoints, such as availability and latency.
   - Alerts are configured to notify administrators of any downtime or performance issues.

---

## How to Run

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   ```

2. **Set Up Jenkins**:
   - Install Jenkins on a server.
   - Configure Jenkins pipeline to integrate with Git, Maven, SonarQube, and Nexus.

3. **Configure SonarQube**:
   - Set up a SonarQube server.
   - Integrate it with Jenkins for static code analysis.

4. **Set Up Nexus**:
   - Configure a Nexus Repository to store build artifacts.

5. **Deploy to AWS EC2**:
   - Launch an EC2 instance.
   - Install required dependencies (e.g., Java, Tomcat).
   - Deploy the application build artifacts to the EC2 server.

6. **Configure Prometheus Blackbox Exporter**:
   - Install and configure Prometheus on a monitoring server.
   - Add targets for monitoring application endpoints.

7. **Use Initial User Data**:
   - Preloaded credentials:
     - **Username**: `bugs`  |  **Password**: `bunny` (User role)
     - **Username**: `daffy` |  **Password**: `duck`  (Manager role)
   - Alternatively, sign up as a new user and customize your role.

---

## Monitoring and Observability

- **Prometheus Blackbox Exporter** ensures that application endpoints are constantly monitored for availability and performance.
- Alerts notify administrators immediately in case of downtime or latency issues.

---

## Benefits of the CI/CD Pipeline

1. **Automation**: Reduces manual effort by automating builds, tests, and deployments.
2. **Code Quality**: Ensures high-quality code with SonarQube analysis.
3. **Artifact Management**: Maintains a repository of build artifacts for version control.
4. **Security and Performance**: Cloudflare provides enhanced security and performance.
5. **Reliability**: Prometheus ensures system reliability with monitoring and alerting.

---

## Conclusion

This **BoardgameListingWebApp** is a robust, full-stack application enhanced with a well-defined CI/CD pipeline for seamless development, testing, deployment, and monitoring. Its integration with tools like Jenkins, SonarQube, Nexus, and Prometheus ensures high-quality code, efficient deployments, and reliable performance.

