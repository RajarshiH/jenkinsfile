pipeline {
    agent any

    stages {
        stage('git') {
            steps {
                git branch: 'dev', credentialsId: 'jenkins-github-id', url: 'https://github.com/RajarshiH/demodevops.git'
                  }
            }
        stage('deploy'){
            steps {
                dir("${WORKSPACE}") {
                    sh 'sudo cp "${WORKSPACE}"/html/index.html /var/www/html/'
                     }
                
            }
            
        }
    }
}
