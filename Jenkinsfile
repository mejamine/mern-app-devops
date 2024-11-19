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
                    sh 'echo root | sudo -S docker build .'
                }
            }
        }
        stage("build server image"){
            steps {
                dir("server"){
                    sh 'echo root | sudo -S docker build .'
                }
            }
        }
    }
}