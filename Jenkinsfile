pipeline {
    agent {
        docker {
            image 'altwalker/altwalker:latest'
            args '-u root:root'
        }
    }
    stages {
        stage('test') {
            steps {
                sh 'python3 -m altwalker online tests -m models/model.json "random(vertex_coverage(100))"'
            }
        }
    }
}
