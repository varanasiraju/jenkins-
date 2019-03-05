pipeline {
    agent any 
    stages {
       stage('Build') {
           step {
               sh 'mvn clean package'
           }
		   step {
		   sh label: '', script: 'docker image build -t docker .'
		   }
       }     

    }  
}

