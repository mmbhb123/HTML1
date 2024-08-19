pipeline {
    agent { 
        node {
            label 'new2'
            }
      }
    stages {
        stage('Build') {
            steps {
                echo "Building.."
                powershell '''
                Write-Host "doing build stuff.."
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                powershell '''
                Write-Host "doing test stuff.."
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                powershell '''
                Write-Host "doing delivery stuff.."
                '''
            }
        }
    }
}
