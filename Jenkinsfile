pipeline {
agent any
  tools {
    jdk 'oraclejdk8'
  }
    stages {
    stage('Set Build Name') {
      steps { 
        echo "Set Build Name"        
        withFolderProperties{
          echo("Crossplane")
          script { 
            currentBuild.displayName = "${BUILD_NUMBER}"
            currentBuild.description = "${BRANCH} - ${GIT_COMMIT}"    
          }    
        }
      }
    } 
	}
	}
   
