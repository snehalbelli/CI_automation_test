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
                    sh "docker build -t greet:v2 ."
                    sh "docker tag greet:v2 snehalbelli/practice:v2"
                }
                }
        }
        stage("push image"){
            steps{
                sh "docker push snehalbelli/practice:v2"
            }
        }
    }
}