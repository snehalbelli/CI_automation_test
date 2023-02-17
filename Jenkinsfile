pipeline{
    agent any
    stages{
        stage("clone repo"){
            steps{
                sh "git clone https://github.com/snehalbelli/CI_automation_test.git"
            }
            
        
        }
        stage("build image"){
            steps{
                dir("CI_automation_test"){
                    sh "ls -al"
                }
                }
        }
        stage("push image"){
            steps{
                sh "docker --version"
            }
        }
    }
}