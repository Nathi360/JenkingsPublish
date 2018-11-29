pipeline {
    agent any
    
    stages {
        stage('B U I L D') {
            steps {
                sh 'ng build --prod'
            }
        }
        stage('T E S T') {
            steps {
                ng test
            }
        }
        stage('T R A N S F E R') {
            steps {
                //Copy '/dist' to CPANEL here!
                echo "Hello!"
            }
        }
    }
    post{
        always{
            echo "terminate FTP connection"
        }
    }
}
