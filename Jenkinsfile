pipeline
{
	agent {label 'AOP'}
options {
	buildDiscarder(logRotator(numToKeepStr: '5'))
}
        stages
	
        {
            stage ('mysonarqubescan') 
            {
                steps { 

			withSonarQubeEnv(installationName: 'mysonarqube')  
			{
				//sh './mvnw clean org.sonarsource.scanner.maven:sonar-maven-plugin:3.9.0.2155:sonar'
				sh 'mvn sonar:sonar'
             	}
                		}
        }
	}
	
}












