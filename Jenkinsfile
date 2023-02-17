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
                    sh "sudo docker build -t greet:v3 ."
                    sh "sudo docker tag greet:v3 snehalbelli/practice:v3"
                }
                }
        }
        stage("push image"){
            steps{
                sh "sudo docker push snehalbelli/practice:v3"
            }
        }
    }
}