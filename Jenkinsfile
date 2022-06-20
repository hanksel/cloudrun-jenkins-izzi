echo 'Se inicio el pipeline'



pipeline {
   agent any



stages {
    stage('Run gcloud') {
        steps {
		        sh "cat /etc/os-release"
		        sh "pwd"
				sh "ls"

                sh "gcloud --version"
				sh "gcloud auth list"
        }
    }
	  
	
    stage('cloud run deploy') {
        steps {
		        sh "gcloud run deploy cloudrun-jenkins --region us-east4 --platform managed --port 3000 --allow-unauthenticated --source ."
        }
    }
    
}
}

echo 'Fin del pipeline'