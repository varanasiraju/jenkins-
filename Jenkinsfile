pipeline {
    agent any 
    stages {
       stage('Build') {
               sh 'mvn clean package'
           }
		stage('docker build'){
		   sh label: '', script: 'docker image build -t docker .'
		   }
       }     

    }  


