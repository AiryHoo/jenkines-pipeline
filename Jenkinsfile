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
		success {
			dingTalk accessToken:'83d77d2f5cfacf44bc2f0601ef05da82b67aa5031e15e68592443cf1e339edbc', 
			imageUrl:'', 
			jenkinsUrl:'http://192.168.248.153:8080/', 
			message:'pipeline success, congratulations~', 
			notifyPeople:''
		}
		failure {
			dingTalk accessToken:'83d77d2f5cfacf44bc2f0601ef05da82b67aa5031e15e68592443cf1e339edbc', 
			imageUrl:'', 
			jenkinsUrl:'http://192.168.248.153:8080/', 
			message:'pipeline fail, go on guys.', 
			notifyPeople:''
		}
	}
}