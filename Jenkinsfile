pipeline {
  agent none

  stages{
    stage('stage branch') {
      agent {
        label 'test-ccpay'
      }
      when {
        branch 'stage'
      }
      steps {
        sh '''
          mkdir -p test
          echo "stage branch"
        '''
    }
      stage('stage branch') {
      agent {
        label 'azure-linux'
      }
      when {
        branch 'main'
      }
      steps {
        sh '''
          mkdir -p prod
          cd configurations
          echo "main branch"
        '''
    }
  }
}
