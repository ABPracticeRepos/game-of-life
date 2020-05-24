pipeline {
    agent{label 'MASTER'}      
    stages {
        stage ('source'){
            steps {
                git 'https://github.com/ABPracticeRepos/game-of-life.git'
            }
        }
        stage('Package'){
            steps {
                sh 'mvn package'
            }
        }
    }
}

node {
    stage('scm') {
        git 'https://github.com/ABPracticeRepos/game-of-life.git'
    }
    stage('build'){
        sh 'mvn package'
    }
}
