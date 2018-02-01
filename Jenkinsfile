pipeline {

    agent any 
    parameters {
        string(name: 'ORGANIZATION', description: 'Apigee Organization')
        string(name: 'ENVIRONMENT', description: 'Apigee Environment')
    }
    stages {
        stage('Test'){
            steps {
                withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'apigee-credentials',
                            usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD']]) {     
                    sh 'echo $params.ORGANIZATION'
                    sh 'gulp -u ${USERNAME} -p ${PASSWORD} -o ${params.ORGANIZATION} -e ${params.ENVIRONMENT} deploy'
                }
            }
        }
    }

}
