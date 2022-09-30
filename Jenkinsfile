pipeline{
    agent any
    stages{
        stage("Pipeline Startup"){
            steps{
                echo "========Pipeline Startup========"
            
            }
        }
        stage('pre packages pipeline') {
            steps {
                echo 'Pre Package Pipeline'
            }
        }
        stage('Docker File') {
            steps {
                echo 'Pre Package Pipeline'
                agent{
                    dockerfile {
                        filename 'Dockerfile.build'
                        dir 'build'
                        label 'my-defined-label'
                        additionalBuildArgs  '--build-arg version=1.0.0'
                        args '-v /tmp:/tmp'
                    }
                }
            }
        }

    }
}
