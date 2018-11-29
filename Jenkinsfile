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
                bat 'npm build --prod'
            }
        }
        stage('T R A N S F E R') {
            steps {
                //Copy '/dist' to CPANEL here!
                bat 'dir'
            }
        }
        stage('T E S T') {
            steps {
                bat 'npm e2e'
            }
        }
    }
    post{
        always{
            echo "terminate FTP connection"
        }
    }
}
