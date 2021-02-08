pipeline{
    agent{
        label 'win'
    }
    tools {
        maven 'mvn3'
        jdk 'jdk11'
        git 'Default'
    }
    stages{
        stage("Checkout SCM"){
            steps{
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/krishna26kulkarni/demo'
            }
        }
        stage("Build"){
            steps{
                sh 'mvn clean install'
            }
        }
    }
}
