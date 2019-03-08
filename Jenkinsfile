pipeline {
    agent any
    stages {
       stage('Build') {
           steps {
		   node('master'){
               sh 'mvn clean package'
			   sh label: '', script: 'sudo docker image build -t devi .'
			   sh label: '', script: 'sudo docker login -u admin -p admin123 52.14.54.48:8888'
			   sh label: '', script: 'sudo docker tag devi:latest 52.14.54.48:8888/devi:1.0.0'
			   sh label: '', script: 'sudo docker push 18.218.171.29:8888/devi:1.0.0'
			   }
		   node('slave1'){	
		       sh label: '', script: 'sudo docker login -u admin -p admin123 52.14.54.48:8888'
		       sh label: '', script: 'sudo docker pull 52.14.54.48:8888/devi:1.0.0'
			   sh label: '', script: 'sudo docker service create --name qt-raju --network qt-overlay --replicas 3  -it -d -p 9999:8080 52.14.54.48:8888/devi:1.0.0'
           }
		}
		
    }  
}
}

