pipeline {
 agent any
 stages {
 stage('Checkout') {
 steps {
 git branch: 'main',
 url: 'https://github.com/ShashankNayakaSP/Dev.git'
 }
 }
 stage('Deploy Website') {
 steps {
 sh '''
 sudo rm -rf /var/www/html/*
 sudo cp -r * /var/www/html/
 '''
 }
 }
 }
 post {
 success {
 echo 'Website deployed successfully'
 }
 failure {
 echo 'Deployment failed'
 }
 }
}
