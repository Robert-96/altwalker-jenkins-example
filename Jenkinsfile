pipeline {
    agent { docker { image 'altwalker/altwalker:latest' } }
    stages {
        stage('test') {
            steps {
                sh 'python -m altwalker online tests -m models/model.json "random(vertex_coverage(100))"'
            }
        }
    }
}
