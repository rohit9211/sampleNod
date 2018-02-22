pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        echo 'test'
      }
    }
    stage('Code Complile') {
      steps {
        echo 'DYNAMO_HOME is "${env.DYNAMO_HOME}"'
        sh '''if [ ${ServerName} == "stage2" ]
	then
	export serverName=stage2
	export serverIP=192.168.130.11

elif [ ${ServerName} == "dev2" ]
	then
	export serverName=dev2
	export serverIP=192.168.130.10

else
	echo "Selected Server is not configured . Please contact Jenkins Administrator"
fi'''
      }
    }
  }
  environment {
    DYNAMO_HOME = '/data/atg/ATG_WL_10.2/home'
    ATG_HOME = '/data/atg/ATG_WL_10.2'
  }
}