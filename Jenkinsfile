pipeline {
agent any
   stages {
	stage('Clone'){
		steps{
		git 'https://github.com/ravindrab5/spring-petclinic.git'
		}
         }
stage('Compile & Package'){
			steps{
        		withMaven(maven :'MAVEN_HOME'){
				sh 'mvn package'
			}
			}
  }
stage('Create databases'){
			steps{
        		sh 'docker-compose up -d'
                        sh 'nohup java -jar target/*.jar'
			}
  }

}
}
