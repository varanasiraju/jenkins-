pipeline {
    agent any
    stages {
       stage('Build') {
           steps {
		   node('master'){
               sh 'mvn clean package'
			   sh label: '', script: 'sudo docker image build -t devi .'
			   sh label: '', script: 'sudo docker login -u admin -p admin123 52.14.54.48:8888'
			   sh label: '', script: 'sudo docker tag devi:latest 52.14.54.48:8888/devi:1.0.1'
			   sh label: '', script: 'sudo docker push 52.14.54.48:8888/devi:1.0.1'
			   }
		}
		
    }  
}
}
  
