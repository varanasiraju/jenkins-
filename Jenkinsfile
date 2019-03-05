pipeline {
    agent any 
    stages {
       stage('Build') {
           steps {
               sh 'mvn clean package' 
           }
		}
		stage ("Build image") {

        dockerfile = docker.build 'my-image:snapshot'
    }
    }  
}

