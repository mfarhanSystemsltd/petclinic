pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'mvn -B -DskipTests clean package'
                sh 'nohup java -Dserver.port=8082 -jar target/*.jar &'
            }
        }
    }
}
