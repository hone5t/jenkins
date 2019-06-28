pipline {
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
}