pipeline {
  agent {
    label 'NODEJS'
    }

  stages {

    stage('prepare Artifacts') {
      steps {
        sh '''
          cd static
          zip -r ../frontend.zip *
        '''
      }
    }
    stage('upload artifacts') {
      steps {
        sh '''
          curl -f -v -u admin:admin123 --upload-file frontend.zip http://172.31.8.88:8081/repository/frontend/frontend.zip
        '''
      }
    }
  }
}