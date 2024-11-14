pipeline {
    agent any

    environment {
        JAVA_HOME = "C:/Program Files/Java/jdk-17"
    }

    stages {
        stage('Clean Stage') {
            steps {
                dir("SimpleMavenProject") {
                    // Clean the project
                    bat 'C:/Users/ShriB/apache-maven-3.9.9/bin/mvn clean -f C:/ProgramData/Jenkins/.jenkins/workspace/ZensarPipelineFromGit/SimpleMavenProject/pom.xml'
                }
            }
        }

        stage('Compile Stage') {
            steps {
                dir("SimpleMavenProject") {
                    // Compile the project
                    bat 'C:/Users/ShriB/apache-maven-3.9.9/bin/mvn compile'
                }
            }
        }

        stage('Install Stage') {
            steps {
                dir("SimpleMavenProject") {
                    // Install the project
                    bat 'C:/Users/ShriB/apache-maven-3.9.9/bin/mvn install'
                }
            }
        }
    }
}