pipeline {
    agent{ label 'MASTER' }      
    triggers { 
        upstream(upstreamProjects: 'sample', threshold: hudson.model.Result.SUCCESS) 
    }
    stages {
        stage ('source'){
            steps {
                git 'https://github.com/ABPracticeRepos/game-of-life.git'
            }
        }
        stage('Package'){
            steps {
                sh 'mvn package'
                input 'Continue to Next Step?'
                archiveArtifacts '/target/*.jar'
            }
        }
    }
}
