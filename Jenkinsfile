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
                $path = "C:\\Users\\Admin\\Documents\\kk\\1.txt"
                if (Test-Path $path) {
                    $newPath = $path -replace ".txt", "-copy.txt"
                    New-Item -Path $newPath -ItemType File
                    Write-Host "Created $newPath"
                } else {
                    New-Item -Path $path -ItemType File
                    Write-Host "Created $path"
                }
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                powershell '''
                $path = "C:\\Users\\Admin\\Documents\\kk\\2.txt"
                if (Test-Path $path) {
                    $newPath = $path -replace ".txt", "-copy.txt"
                    New-Item -Path $newPath -ItemType File
                    Write-Host "Created $newPath"
                } else {
                    New-Item -Path $path -ItemType File
                    Write-Host "Created $path"
                }
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Delivering...'
                powershell '''
                $path = "C:\\Users\\Admin\\Documents\\kk\\3.txt"
                if (Test-Path $path) {
                    $newPath = $path -replace ".txt", "-copy.txt"
                    New-Item -Path $newPath -ItemType File
                    Write-Host "Created $newPath"
                } else {
                    New-Item -Path $path -ItemType File
                    Write-Host "Created $path"
                }
                '''
            }
        }
    }
}
