pipeline{
    agent any
    stages{
        stage('stage-paralle'){
            parallel{
                stage('sub-job1'){
                    steps{
                        echo "sub-job1 tasl"
                    }
                }
                stage('sub-job2'){
                    steps{
                        echo "sub-job2 task"
                    }
                }
            }
        }
        stage('version-check'){
            steps{
                echo "end of the parallel job"
            }
        }
    }
}
