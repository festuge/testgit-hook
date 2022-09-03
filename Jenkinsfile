pipeline{
    agent any
    stages{
        stage('git-clone'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-id', url: 'https://github.com/festuge/testgit-hook.git']]])
            }
        }
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
                stage('user-check'){
                    steps{
                        sh 'cat /etc/passwd | grep jenkins'
                    }
                }
            }
        }
        stage('version-check'){
            steps{
                echo "end of the parallel job"
            }
        }
        stage('webhook-fix'){
            steps{
                echo "webhook fixed"
            }
        }
    }
}
