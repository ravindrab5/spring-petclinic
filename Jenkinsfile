pipeline {
agent any
   stages {
	stage('Clone'){
		steps{
		git 'https://github.com/ravindrab5/maven-project.git'
		}
         }
stage('Compile & Package'){
			steps{
        		withMaven(maven :'MAVEN_HOME'){
				sh 'mvn package'
			}
			}
  }

}
}
