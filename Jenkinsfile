pipeline {
    agent any 
    stages {
       stage('Build') {
           steps {
               sh 'mvn clean package'
			   sh label: '', script: 'sudo docker image build -t raju .'
           }
		}
		
    }  
}

