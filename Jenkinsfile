pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build completed'
      }
    }

    stage('Test stages') {
      parallel {
        stage('Test2') {
          steps {
            echo 'Running Test2'
          }
        }

        stage('Test1') {
          steps {
            echo 'Running Test1'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Are you sure to deploy ?', ok: 'Yes !')
        echo 'deployment completed'
      }
    }

    stage('Notify for new build') {
      steps {
        echo 'build completed successfully'
      }
    }

  }
}