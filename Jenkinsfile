node('master'){
        stage('Code Checkout'){
		checkout scm
	}
	stage('Build Automation'){
		sh "mvn clean install -Dmaven.test.skip=true"
	}
	stage('Archieve Artifacts'){
	       archieveArtifacts artifacts: 'target/*.war'
	}
        stage('Code Deployment'){
	        //deploy adapters: [tomcat9(credentialsId: 'TomcatCreds', path: '', url: 'http://3.80.62.202:8080//')], contextPath: 'Planview', onFailure: false, war: 'target/*.war'
	}
}
