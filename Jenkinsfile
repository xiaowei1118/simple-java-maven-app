pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args '-v /Users/zhengzhihao/.m2:/root/.m2'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'sh \'mvn -B -DskipTests clean package\''
      }
    }
    stage('Test') {
      steps {
        sh 'sh \'mvn test\''
      }
    }
  }
}