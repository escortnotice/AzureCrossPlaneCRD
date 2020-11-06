pipeline {
agent any
    stages {
    stage('Set Build Name') {
      steps { 
        echo "Set Build Name"        
          echo("Crossplane")
          script { 
            currentBuild.displayName = "${BUILD_NUMBER}"
            currentBuild.description = "${GIT_COMMIT}"    
            sh '''#!/bin/bash 
	    kubectl get pods
		'''
        }
      }
    } 
 }
}
