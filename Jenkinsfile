pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh ("sudo su")
                sh ("sudo docker cp /var/lib/jenkins/workspace/git-pull/hello.html mynginx1:/usr/share/nginx/html/index.html")
            }
        }
        stage('Test') {
            steps {
                sh 'echo $(curl localhost:8080)'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
