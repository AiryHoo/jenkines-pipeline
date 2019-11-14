Jenkinsfile (Declarative Pipeline)
pipeline {
    agent {
        docker {
             image 'hashicorp/terraform:0.12.12'
             args '--entrypoint=""'
        }
    }
    stages {
        stage("envInit"){
            steps {
                sh 'echo "terraform init..."'
            }
        }
        stage('build') {
            steps {
                sh 'echo "build..."'
            }
        }
        stage('deploy') {
            steps {
                sh 'echo "deploy..."'
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
}
