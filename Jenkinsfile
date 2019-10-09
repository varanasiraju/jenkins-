pipeline {
    agent any
    stages {
       stage('Build') {
           steps {
		   node('master'){
                        sh 'mvn clean package'
			sh label: '', script: 'java -jar target/*.jar'   
			   }
		   
		}
		
    }  
}
}
  
