pipeline {
    agent any
    stages {
        stage('pipeline startup') {
            steps {
                echo 'Pipeline Start up'
            }
        }
        stage('pre packages pipeline') {
            steps {
                echo 'Pre Package Pipeline'
            }
        }
        stage('package analysis') {
            steps {
                echo 'Analysis'
            }
        }
        stage('maven') {
            steps {
                echo 'Mave Build'
            }
        }
        stage('build') {
            steps {
                echo 'sct'
            }
        }
        stage('Checkout') {
        when {
            allOf {
                not { changeset pattern: "Jenkinsfile" }
                branch 'master'
            }    
        }
        steps {
            echo 'Checkout'
        }
    }
        stage('sonar check') {
            steps {
                echo 'sct'
            }
        }
        stage('deployed') {
            steps {
                echo 'sct'
            }
        }
    }
}
