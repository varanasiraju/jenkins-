pipeline {
    agent any
    stages {
       stage('Build') {
           steps {
		   node('master'){
               sh 'mvn clean package'
			   sh label: '', script: 'sudo docker image build -t devi .'
			   sh label: '', script: 'sudo docker login -u admin -p admin123 18.218.171.29:8888'
			   sh label: '', script: 'sudo docker tag devi:latest 18.218.171.29:8888/devi:1.0.0'
			   sh label: '', script: 'sudo docker push 18.218.171.29:8888/devi:1.0.0'
			   }
		   node('slave1'){	
		       sh label: '', script: 'sudo docker login -u admin -p admin123 18.218.171.29:8888'
		       sh label: '', script: 'sudo docker pull 18.218.171.29:8888/devi:1.0.0'
			   sh label: '', script: 'sudo docker container run -it -d -p 9999:8080 18.218.171.29:8888/devi:1.0.0'
           }
		}
		
    }  
}
}

