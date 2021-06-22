pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
               bat "git clone https://github.com/LunaMorena9/docker-jenkins-example.git"
               bat "mvn clean -f docker-jenkins-example"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f docker-jenkins-example"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f docker-jenkins-example"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f docker-jenkins-example"
            }
        }
    }
}