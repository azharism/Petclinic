pipeline {
    agent any
    
    tools{
        jdk 'jdk11'
        maven 'maven3'
        
    }

    stages {
        stage('git checkout') {
            steps {
                git branch: 'feature-2', url: 'https://github.com/azharism/Petclinic.git'
            }
        }
        stage('compile') {
            steps {
                sh "mvn clean compile"
            }
        }
        stage('build') {
            steps {
                sh "mvn clean package -DskipTests=true"
            }
        }
          
    }
}
