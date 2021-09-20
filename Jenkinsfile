pipeline {
    agent { docker { image 'altwalker/altwalker:latest' } }
    stages {
        stage('test') {
            steps {
                sh 'pip install -r requirements.txt --user'
                sh 'altwalker online tests -m models/model.json "random(vertex_coverage(100))"'
            }
        }
    }
}
