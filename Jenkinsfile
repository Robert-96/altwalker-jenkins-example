pipeline {
    agent { docker { image 'altwalker/altwalker:latest' } }
    stages {
        stage('test') {
            steps {
                sh 'sudo python3 -m pip install --upgrade pip'
                sh 'sudo python3 -m install -r requirements.txt'
                sh 'altwalker online tests -m models/model.json "random(vertex_coverage(100))"'
            }
        }
    }
}
