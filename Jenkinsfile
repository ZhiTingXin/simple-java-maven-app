#!/groovy
pipeline {
    agent {
        docker {
            image 'maven:3.6.3'
            args '-v /root/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'pwd'
                sh 'whereis java'
                sh 'mvn -v'
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }

}
