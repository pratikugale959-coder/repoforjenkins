pipeline {
  agent any
  stages{
    stage('Build')    { steps { bat 'echo Building the project' } }
    stage('Test')     { steps { bat 'echo Running tests' } }
  }
  post {
    success { echo 'All stages passed' }
  }
}
