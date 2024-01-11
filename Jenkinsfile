pipeline{
    agent any

    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github_java', url: 'https://github.com/ayoubon1/maven']]])
            }
        }
        stage('build'){
            steps{
               bat 'mvn package'
            }
        }
    }
}
