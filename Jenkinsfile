// Powered by Infostretch 

timestamps {

node () {

	stage ('App-IC - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'git-login', url: 'https://github.com/AzaiezMohamedAmine/jenkins-sample.git']]]) 
	}
	
	stage('Quality check') {
        withSonarQubeEnv('Sonar') {
        bat "mvn verify org.sonarsource.scanner.maven:sonar-maven-plugin:sonar -Dsonar.projectKey=jenkins-demoTest"
}
}
}
}
