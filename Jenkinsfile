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
       stage("build & SonarQube analysis") {
          node {
              withSonarQubeEnv('My SonarQube Server') {
                 sh 'mvn clean package sonar:sonar'
              }
          }
      }

      stage("Quality Gate"){
          timeout(time: 1, unit: 'HOURS') {
              def qg = waitForQualityGate()
              if (qg.status != 'OK') {
                  error "Pipeline aborted due to quality gate failure: ${qg.status}"
              }
          }
      }
        stage('deployed') {
            steps {
                echo 'sct'
            }
        }
        stage('Prod') {
            steps {
                echo 'sct'
            }
        }
    }
}
