pipeline {

    agent {
        node { 
            withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'apigee-credentials',
                        usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD']])     

        }
    }
	stages {
        stage('Test'){

            sh 'echo $USERNAME'

        }
    }

}
