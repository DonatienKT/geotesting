pipeline{
    agent any 
    tools{
        maven 'M2_HOME'
    }
    stages {
    stage ('clean'){
        steps{
            sh 'mvn clean'
        }
    }
    stage('install'){
        steps{
            sh 'mvn install'
        }
    }
 stage('package all'){
        steps{
            sh 'mvn package'
        }
    }

    }
}