# Hello Java Maven + Jenkins CI

This is a simple Java "Hello World" project built using Maven and integrated with Jenkins for continuous integration (CI).

## Objective

Demonstrate how to:
- Create a Java application using Maven
- Configure a Jenkins Freestyle project to build it
- Verify successful build using Maven goals

## Project Structure

hello-java-maven/ ├── pom.xml └── src/ └── main/ └── java/ └── HelloWorld.java

## Technologies Used

- Java 1.8
- Maven 3.8.x
- Jenkins LTS
- Git & GitHub

## Jenkins Build Configuration

- Type: Freestyle project
- SCM: Git (connected to this repository)
- Build Step: Invoke top-level Maven targets
  - Goals: `clean package`

## Build Output Screenshot

Below is the screenshot of a successful Jenkins build showing `BUILD SUCCESS` and `Finished: SUCCESS`.

build_success.png

## How to Run Locally

1. Clone the repository:
git clone https://github.com/GOURIDO/hello-java-maven.git

2. Navigate to the project folder:
cd hello-java-maven

3. Build the project using Maven:
mvn clean package

4. Run the program:
java -cp target/hello-1.0.jar HelloWorld

## Tech Stack

- Programming Language: Java 1.8
- Build Tool: Apache Maven 3.8.x
- CI/CD Tool: Jenkins LTS
- Version Control: Git
- Hosting: GitHub
