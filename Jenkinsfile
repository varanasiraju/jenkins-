pipeline {
    agent any 
    stages {
       stage('Build') {
           steps {
               sh 'mvn clean package' 
           }
		}
		stage ("Build image") {

        myImg = docker.build 'my-image:snapshot'
    }
    }  
}

