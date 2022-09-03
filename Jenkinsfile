pipeline{
    agent any
    stages{
        stage('1-parallel-level){
            parallel{
                stage('sub-job'){
                    steps{
                        echo "sub-job1 talk"
                    }
                }
                stage('sub-job'){
                    steps{
                        echo "sub-job2 talk"
                    }
                }
            }
        }
        stage('version-check'){
            steps{
                echo "end of parallel job"
            }
        }
    }
}
