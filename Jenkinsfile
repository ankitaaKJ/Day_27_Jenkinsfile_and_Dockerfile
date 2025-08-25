pipeline{
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t sample-httpd-img:latest .'
           }
        }

        stage('Run Container'){
            steps{
                sh 'docker run -dp 1000:80 sample-httpd-img:latest'
            }
        }

        stage('Check Running Containers'){
            steps{
                sh 'docker ps'
            }
        }
  }
}
