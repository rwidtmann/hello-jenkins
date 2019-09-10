pipeline {
    agent any

    stages {

        stage('build') {
            steps {
              sh '''
                 ./mvnw -DskipTests clean compile
              '''
            }
        }

        stage('test') {
            steps {
              sh '''
                     ./mvnw test
              '''
            }
        }

        stage('deliver') {
            steps {
              sh '''
                     ./mvnw -DskipTests install
              '''
            }
        }

    }
}
