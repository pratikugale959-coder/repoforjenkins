pipeline {
  agent any 
  parameters { choice(name: 'ENVIRONMENT',
                        choices: ['staging', 'production']) 
             }
  stages {
    stage('Checkout') { steps { checkout scm } }
    stage('quality') { parallel {
      stage('Build') { steps { bat 'echo build'} }
      stage('Lint') { steps { bat 'echo lint'} }
    }
                     }
    stage('Test')  { steps { bat 'echo test' } }
    stage('Package') { steps { bat 'echo package'} }
  }
}
