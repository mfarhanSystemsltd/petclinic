pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'mvn -B -DskipTests clean package'
                sh 'java -Dserver.port=8888 -jar target/*.jar '
            }
        }
    }
}