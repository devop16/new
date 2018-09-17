pipeline {
  agent any
  stages {
    stage('Dev') {
      steps {
        echo 'Push to next step'
      }
    }
    stage('DevOps Approval') {
      steps {
        echo 'Sucess'
      }
    }
    stage('QA') {
      steps {
        echo 'Push to next step'
      }
    }
    stage('security steps') {
      parallel {
        stage('DevOps Approval') {
          steps {
            echo 'Sucess'
          }
        }
        stage('Validator') {
          steps {
            echo 'Sucess'
          }
        }
      }
    }
    stage('Production') {
      steps {
        echo 'Predeployment steps compelete'
      }
    }
  }
}