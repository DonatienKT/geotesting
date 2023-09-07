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
            nexusArtifactUploader artifacts: [[artifactId: 'bioMedical', classifier: '',
            file: 'target/bioMedical-0.0.3-SNAPSHOT.jar', type: 'war']],
             credentialsId: 'NEXUSID', groupId: 'qa',
                nexusUrl: '198.58.119.40:8081', nexusVersion: 'nexus3', protocol: 'http',
                repository: 'donas_war-file', version: '0.0.4-SNAPSHOT'
        }
    }
    }
}

