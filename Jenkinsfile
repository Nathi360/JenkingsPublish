pipeline {
    agent any
    
    stages {
		stage('S E T U P') {
            steps {
				bat 'npm install -g @angular/cli'
                bat 'npm install'
            }
        }
        stage('B U I L D') {
            steps {
                bat 'npm run-script build --prod'
            }
        }
        stage('T E S T') {
            steps {
                bat 'npm e2e'
            }
        }
        stage('C H E C K') {
            steps {
                //Copy '/dist' to CPANEL here!
                bat 'dir'
            }
        }
    }
    post{
        always{
            echo "terminate FTP connection"
        }
    }
}
