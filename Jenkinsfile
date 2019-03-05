pipeline {
    agent any 
    stages {
       stage('Build') {
           steps {
               sh 'mvn clean package'
			   sh 'sudo docker build -f dockerfile . -t image' 
           }
		}
		
    }  
}

