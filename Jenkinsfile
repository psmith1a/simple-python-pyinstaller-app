pipeline {
  agent none
  stages {
    stage('Build') {
      agent {
        docker {
          image 'python:2-alpine'
        }

      }
      steps {
        sh 'sh \'python -m py_compile sources/add2vals.py sources/calc.py\''
      }
    }
    stage('Test') {
      steps {
        sh 'sh \'py.test --verbose --junit-xml test-reports/results.xml soures/test_calc.py\''
      }
    }
  }
}