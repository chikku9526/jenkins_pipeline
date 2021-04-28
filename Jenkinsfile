pipeline {
  agent any
	environment {
		def PROJECT_NAME_DEPLOY = "ISSClsServer_Deployment"
		def DEPLOYMENT_URL = "https://github.com/chikku9526/ISSClsServer_Deployment.git"
		def FileName = "issclsserver"
		def screeName = "dmt"
		
		
	}
	
  stages {
        stage("update server name") {
            steps {
                script {
                    sh "ls -ltr"
			sh "set +x; git clone https://${GIT_USERNAME}:${PASSWORD}@${DEPLOYMENT_URL}; set -x "
                    sh "ls -ltr"
		    sh "cd ${PROJECT_NAME_DEPLOY}"
		    sh "ls -ltr"
		    sed '/^<destination id/d' ${FileName}-${params.DESTINATION}-deployment.xml
		    for (String dest : params.SERVERS.split("\n")) {
			sh """
				sed -i '7 i <destination id="DEST.ground.chikku.com" hostAndDirectory="DEST.ground.chikku.com:/app/localstorage/SCREEN" setId="Set1"></destination>'
				sed -i "s|DEST|$dest|g" ${FileName}-${params.DESTINATION}-deployment.xml
				sed -i "s|SCREEN|$screeName|g" ${FileName}-${params.DESTINATION}-deployment.xml
			"""
		    }
		   	sh """
				git add -A
                		git commit -m " Pushed Repo setup files to branches on \$(date) "
                		set +x
                		git push https://${GIT_USERNAME}:${PASSWORD}@${DEPLOYMENT_URL} \main > /dev/null 2>&1
                		set -x
						
                }
            }
        }
    }

