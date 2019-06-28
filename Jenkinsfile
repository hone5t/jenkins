pipeline {
    agent { docker {image 'python:3.7.2'}}
    stages {
        stage('build') {
            steps {
                sh 'python --version'
                sh 'echo "Hello World"'
                sh '''
                    echo "and multiline shell stops work too"
                    ls -lah
                    '''
            }
        }
    }
    post {
        always {
            echo "posting section lets see the result"
        }
        success {
            echo "you didi it"
        }
        failure {
            echo 'well this is failed for some reason'
        }
        unstable {
            echo 'not sure why something become unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'            
        }
    }
}