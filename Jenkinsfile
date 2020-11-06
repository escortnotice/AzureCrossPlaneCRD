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
	    alias kubectl=/usr/local/bin/kubectl
	    kubectl config view
	    echo ("current context ---- ")
	    kubectl config current-context
		'''
        }
      }
    } 
 }
}
