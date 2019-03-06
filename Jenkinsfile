pipeline {
    agent {
  label {
        label "slave1"
  }
} 
    stages {
       stage('Build') {
           steps {
               sh 'mvn clean package'
			   sh label: '', script: 'sudo docker image build -t raju .'
			   sh label: '', script: 'sudo docker container run -it -d -p 8888:8080 raju:latest '
           }
		}
		
    }  
}

