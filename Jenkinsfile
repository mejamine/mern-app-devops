pipeline {
    agent any
    environment {
        IMAGE_NAME_SERVER = "mejbri1998/mern-server"
        IMAGE_NAME_CLIENT = "mejbri998/mern-client"
    }
    stages {
        stage("checkout"){
            steps {
                checkout scm
            }
        }
        stage("build client image"){
            steps {
                dir("client"){
                    sh 'echo root | sudo -S docker build -t mejbri1998/client:1.0 .'
                }
            }
        }
        stage("build server image"){
            steps {
                dir("server"){
                    sh 'echo root | sudo -S docker build -t mejbri1998/server:1.0 .'
                }
            }
        }
        stage("push images to dockerhub"){
            steps{
                sh 'echo root | sudo -S docker push mejbri1998/server:1.0'
                echo 'done push server'
                sh 'echo root | sudo -S docker push mejbri1998/client:1.0'
                echo 'done push client'
            }
        }
    }
}