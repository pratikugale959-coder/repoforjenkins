pipeline {
    agent any 
    parameters  {
        choice (name: 'Environment', choices: ['staging', 'production'],
                description: 'Target')
    }
    stages {
        stage('Tests') {
            parallel {
                stage('Unit') { steps { bat 'echo Unit tests' } }
                stage('integration') { steps { bat 'echo Integration tests' } }
            }
        }
        stage('Package') { steps { bat 'package.bat' } }
        
     post {
            success { archiveArtifacts artifacts: 'dist/**' }
            failure { echo 'CI pipeline failed' }
        }
    }
}
