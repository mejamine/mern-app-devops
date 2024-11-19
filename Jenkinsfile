pipeline {
    agent any
    environment {
        IMAGE_NAME_SERVER = "mejbri1998/mern-server"
        IMAGE_NAME_CLIENT = "mejbri998/mern-client"
    }
    stages {
        stage("checkout"){
            steps {
                git branch 'main',
                url : 'https://github.com/mejamine/mern-app-devops.git'

            }
        }
        stage("build client image"){
            steps {
                dir("client"){
                    sh 'echo root | sudo -S docker build'
                }
            }
        }
        stage("build client image"){
            steps {
                dir("server"){
                    sh 'echo root | sudo -S docker build'
                }
            }
        }
    }
}