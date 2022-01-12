pipeline {
    agent any
    stages {
        stage('Build') {
			environment {
				ANYPOINT_CREDENTIALS = credentials('wp.anypoint.credentials')
			}
            steps {
                bat "mvn clean install deploy -DmuleDeploy -Dusername=${ANYPOINT_CREDENTIALS_USR} -Dpassword=${ANYPOINT_CREDENTIALS_PSW} -Denvironment=Sandbox -DworkerType=Micro -Dworkers=1 -Dregion=us-west-2"
            }
        }
    }
}