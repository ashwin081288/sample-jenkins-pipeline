pipeline{
    agent any
    stages{
        stage("Pipeline Startup"){
            steps{
                echo "========Pipeline Startup========"
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
