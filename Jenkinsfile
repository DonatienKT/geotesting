pipeline{
    agent any 
    stages {
    stage ('hello'){
        steps{
            sh 'echo Hello'
        }
    }
    stage('build'){
        steps{
            sh 'echo hi'
        }
    }
 stage('deploy'){
        steps{
            sh 'echo deployment'
        }
    }

    }
}