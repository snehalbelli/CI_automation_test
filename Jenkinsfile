pipeline{
    agent any
    stages{
        stage("clone repo"){
            steps{
                sh "rm -rf CI_automation_test"
                sh "git clone https://github.com/snehalbelli/CI_automation_test.git"
            }
            
        
        }
        stage("build image"){
            steps{
                dir("CI_automation_test"){
                    sh "sudo docker build -t greet:v2 ."
                    sh "sudo docker tag greet:v2 snehalbelli/practice:v2"
                }
                }
        }
        stage("push image"){
            steps{
                sh "sudo docker push snehalbelli/practice:v2"
            }
        }
    }
}