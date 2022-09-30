pipeline{
    agent any
    stages{
        stage("Pipeline Startup"){
            steps{
                echo "========Pipeline Startup========"
                agent{
                    docker{
                        images 'ashwin081288/department-service:tagname'
                    }
                }
            }
        }
    }
}
