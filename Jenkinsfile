/*pipeline {
    agent{label 'MASTER'}      # You can mention specific Agent Name or as any 
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
*/

#This is first Pipeline changed
node {
    stage('scm') {
        git 'https://github.com/ABPracticeRepos/game-of-life.git'
    }
    stage('build'){
        sh 'mvn package'
    }
}
