pipeline {
    agent any
    stages {
        stage('IQ Source Scan') {
            steps {
                nexusPolicyEvaluation(iqApplication: "${env.JOB_BASE_NAME}", iqStage: 'source')
            }
        }
    }
}