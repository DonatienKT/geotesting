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
 stage('upload artifact'){
        steps{
            sh 'curl --upload-file target/bioMedical-0.0.4-SNAPSHOT.jar -u admin:devops -v http://198.58.119.40:8081/repository/donas_war-file/'
        }
    }
    }
}