pipeline{
    agent any
    tools{
        git 'Default'
        maven 'maven'
    }
     triggers{
        githubPush()
    }
    stages{
        stage("build"){
            steps{
                sh 'mvn clean package'
            }
        }
        stage("archive artifact"){
            steps{
                archiveArtifacts artifacts: '**/*.war'
            }
        }
    }
}
