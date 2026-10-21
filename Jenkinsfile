pipeline {
  agent any
  environment { APP_NAME = 'demo' )
  stages {
    stages('Build') {
      environment { BUILD_MODE = 'production' }
      steps {
        bat 'echo %APP_NAME% %BUILD_MODE%'
      }
    }
  }
}
