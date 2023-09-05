pipeline{
    agent any 
    stages {
    stage ('clean'){
        steps{
            sh '/opt/maven/bin/mvn clean'
        }
    }
    stage('install'){
        steps{
            sh '/opt/maven/bin/mvn install'
        }
    }
 stage('package'){
        steps{
            sh '/opt/maven/bin/mvn package'
        }
    }

    }
}