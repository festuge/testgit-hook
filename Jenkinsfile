pipeline{
    agent any
    stages{
        stage('1-etc_passwd'){
            steps{
                sh 'cat /etc/passwd'
            }
        }
        stage('1-disc_space'){
            step{
                sh 'lsblk'
            }
        }
        stage('1-add_to_file'){
            step{
                echo "I am getting there" >> listics.sh
                sh 'sudo chmod +x listics.sh'
                sh 'listics.sh'
            }
        }
    }
}
