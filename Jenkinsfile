pipeline {
    agent { docker { image 'altwalker/altwalker:latest' } }
    stages {
        stage('test') {
            steps {
                sh 'python3 -m venv .venv'
                sh 'source .venv/bin/activate'
                sh 'pip install --upgrade pip'
                sh 'pip install -r requirements.txt'
                sh 'altwalker online tests -m models/model.json "random(vertex_coverage(100))"'
            }
        }
    }
}
