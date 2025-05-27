pipeline {
  /*
   * TODO: Implement pipeline stages/steps
   *   See documentation: https://www.jenkins.io/doc/book/pipeline/syntax/#stages
   */
   agent any

    stages {
        stage('Build') {
            steps {
                echo 'Running Build...'
                sh './gradlew assemble'
            }
        }
        stage('Test') {
            steps {
                echo 'Running Tests...'
                sh './gradlew test'
            }
        }
    }

    post {
        always {
            junit 'build/test-results/test/*.xml'
        }
    }
}
