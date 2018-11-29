pipeline {
    agent any
    
    stages {
        stage('B U I L D') {
            steps {
                ng build
            }
        }
        stage('T E S T') {
            steps {
                ng test
            }
        }
        stage('D E P L O Y') {
            steps {
                //Copy '/dist' to CPANEL here!
            }
        }
    }
    post{
        always{
            //house-keeping
        }
    }
}
