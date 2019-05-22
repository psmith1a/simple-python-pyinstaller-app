pipeline {
  agent none
  stages {
    stage('Build') {
      steps {
        sh 'sh \'python -m py_compile sources/add2vals.py sources/calc.py\''
      }
    }
  }
}