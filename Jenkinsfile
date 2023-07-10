pipeline {
    agent any
    tools {
        maven 'M2_HOME'
    }

    stages {
        stage('build') {
            steps {
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
            }
        }
        stage('check') {
            steps {
                echo 'Hello check'
                sh 'pwd'
            }
        }
        stage('test') {
            steps {
                echo 'Hello test'
                sh 'docker ps'
            }
        }
    }

post {
        always {
            echo "Always display this message "
        }
        failure {
            echo "Job failed "
        }
        success {
            echo "Successful run "
        }
        unstable {
            echo "The job is unstable "
        }
    
    }
}
