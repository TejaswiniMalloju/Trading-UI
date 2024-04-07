pipeline {
    agent any
      

    stages {
        stage('Git checkout') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/TejaswiniMalloju/Trading-UI.git'
                   }
}
        stage('Install npm prerequisites'){
            steps{
                sh'ng audit fix'
                sh'ng install'
                sh'ng run build'
                sh'cd /var/lib/jenkins/workspace/Trading-ui-pipeline/build'
                sh'pm2 --name Trading-UI start ng -- start'
            }
        }
    }
}
