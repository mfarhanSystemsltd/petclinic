pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'kill -9 $(lsof -t -i:8082) || echo "Process was not running."'
                sh 'mvn -B -DskipTests clean package'
//                 sh 'nohup java -Dserver.port=8082 -jar target/*.jar > log.log 2>&1 &'
                sh 'echo "java -Dserver.port=8082 -jar target/*.jar" | at now + 1 minutes'
//                 sh 'test -f application.pid && xargs kill < application.pid || echo "App was not running, nothing to stop"'
//                 sh 'nohup java -Dserver.port=8082 -jar target/*.jar &'
            }
        }
    }
}
