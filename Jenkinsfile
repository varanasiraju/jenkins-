pipeline {
    agent any 
    stages {
       stage('Build') {
           steps {
               sh 'mvn clean package'
			   sh label: '', script: 'docker image build -t raju .'
           }
		}
		
    }  
}

