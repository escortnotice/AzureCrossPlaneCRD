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
	    echo "current context ---- "
	    kubectl config current-context
	    echo "Applying crd ---- "
	    kubectl apply -f definition.yaml
	    kubectl apply -f composition.yaml
	     kubectl apply -f claim.yaml
	     
		'''
        }
      }
    } 
 }
}
