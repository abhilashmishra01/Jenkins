pipeline {
    tools{
        jdk 'JAVA_HOME_MASTER'
        maven 'M2_HOME_MASTER'
    }
    agent any

    stages {
        stage('git clone') {
            steps {
                git 'https://github.com/abhilashmishra01/Jenkins.git'
                echo 'git cloned successfully'
            }
        }
         stage('compile') {
            steps {
                sh 'mvn compile'
                echo 'successfully build the code'
            }
        }
         stage('unit testing') {
            steps {
                sh 'mvn test'
                echo 'successfully unit testing done'
            }
        }
         stage('package') {
            steps {
                sh 'mvn package'
                echo 'successfully packeged'
            }
        }
    }
}
