pipeline{
    agent {label 'Renat-Agent'}
    stages{
        stage("Restore dependencies"){
            steps{
            sh 'npm install'
            }
        }
        stage("Test"){
            steps{
            sh 'npm run test'
            }
        }
        stage("Build"){
            steps{
            sh 'npm run build'
            }
        }
        stage("Archive Artifacts"){
            steps{
                archiveArtifacts '*.zip'
            }
        }
    }
}
