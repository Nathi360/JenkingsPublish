pipeline {
    agent any
    
    stages {
		    stage('S E T U P') {
            steps {
                bat 'npm install'
            }
        }
        stage('B U I L D') {
            steps {
                bat 'ng build --prod'
            }
        }
        stage('T E S T') {
            steps {
                bat 'ng test'
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
