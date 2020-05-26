pipeline {
    agent{ label 'MASTER' }      
    triggers { 
        upstream(upstreamProjects: 'sample', threshold: hudson.model.Result.SUCCESS) 
    }

    parameters {
        string (name: 'BRANCH_FOR_BUILD',
                defaultValue:'master',
                description:'Enter the branch to be built')          
    }
   
    stages {
        stage ('source'){
            steps {
                git url 'https://github.com/ABPracticeRepos/game-of-life.git', branch: "${param:BRANCH_FOR_BUILD}"
            }
        }
        stage('Package'){
            steps {
                sh 'mvn package'
                
            }
        }
    }
}

