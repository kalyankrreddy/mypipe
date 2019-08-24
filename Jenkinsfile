node {

    stage('Checkout') {
        checkout scm
    }

    stage('Build'){
        sh "mvn clean install"
    }

    stage('Artifact'){
        sh """
		mkdir workbench
		cd target
		zip workbench/my-app-1.0-SNAPSHOT.jar.zip my-app-1.0-SNAPSHOT.jar
		""""
    }

}
