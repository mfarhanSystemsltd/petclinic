pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'mvn -B -DskipTests clean package'
                sh 'java -jar target/*.jar -Dserver.port=8888'
            }
        }
    }
}