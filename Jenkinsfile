pipeline {
  agent any
  stages {
    stage('test') {
      parallel {
        stage('test') {
          steps {
            sh 'echo "test"'
            sh 'echo "test"'
            sh 'echo "test"'
          }
        }

        stage('test linux') {
          steps {
            sh 'echo "test"'
          }
        }

        stage('test windows') {
          steps {
            sh 'echo "test windows"'
            sh 'echo "test windows"'
          }
        }

      }
    }

    stage('verify') {
      steps {
        fileExists 'pom.xml'
        sh 'ls -la'
      }
    }

    stage('build') {
      steps {
        sh 'mvn clean install'
      }
    }

    stage('publish reports') {
      steps {
        echo 'publish'
      }
    }

    stage('deploy') {
      steps {
        sh 'echo "installer le plugin deploy war/ear to a container"'
      }
    }

  }
}