
![Java](https://img.shields.io/badge/Java-8-007396?logo=java&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-3.8.1-1565C0?logo=apache-maven&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-CI%2FCD-D24939?logo=jenkins&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Containerization-2496ED?logo=docker&logoColor=white)
![Build Status](https://img.shields.io/badge/Build-Passing-4CAF50?logo=githubactions&logoColor=white)


# 🚀 Hello World Java Maven - CI/CD using Jenkins

This project demonstrates a simple Java application built using Maven and integrated with Jenkins for continuous integration and deployment.

---

## 🧰 Tech Stack

- **Java 8**: Programming language.
- **Maven**: Build automation tool.
- **Jenkins**: CI/CD automation server.
- **Docker**: Containerization platform.

---

## 🛠️ Jenkins CI/CD Pipeline

### 🔁 Workflow Overview

1. **Code Checkout**: Jenkins pulls the latest code from GitHub.
2. **Build**: Jenkins builds the project using Maven:
    ```bash
    mvn clean package
    ```
3. **Artifact Generation**: A `.jar` file is created in the `target/` directory.
4. **Execution**: The generated `hello-1.0.jar` can be executed with:
    ```bash
    java -jar hello-1.0.jar
    ```

---

### ✅ Maven Configuration (`pom.xml`)

The `pom.xml` file is configured to package the application as a JAR and specify the main class:

```xml
<project xmlns="http://maven.apache.org/POM/4.0.0" ... >
  <modelVersion>4.0.0</modelVersion>
  <groupId>com.example</groupId>
  <artifactId>hello</artifactId>
  <version>1.0</version>
  <packaging>jar</packaging>

  <build>
     <plugins>
        <plugin>
          <groupId>org.apache.maven.plugins</groupId>
          <artifactId>maven-jar-plugin</artifactId>
          <version>3.2.0</version>
          <configuration>
             <archive>
                <manifest>
                  <mainClass>HelloWorld</mainClass>
                </manifest>
             </archive>
          </configuration>
        </plugin>
     </plugins>
  </build>
</project>
```

---

### 📂 Directory Structure (Post-Build)

```
.
├── pom.xml
├── src
│   └── main
│       └── java
│           └── HelloWorld.java
└── target
     └── hello-1.0.jar
```

---

## 📸 Screenshots

### 1️⃣ Jenkins Job Configuration
![Jenkins Job Config](<Screenshot 2025-04-18 120441.png>)
![Jenkins Job Config](<Screenshot 2025-04-18 120534.png>)

### 2️⃣ Successful Build Console Output
![Console Output](<Screenshot 2025-04-18 120626.png>)

### 3️⃣ Application Output
Output of running the JAR file:
![Application Output](image.png)

---
