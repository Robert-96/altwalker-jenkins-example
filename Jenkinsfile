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
                sh 'altwalker --version'
                sh 'altwalker online tests -m models/model.json "random(vertex_coverage(100))" --report-xml'
                junit 'report.xml'
            }
        }
    }
}
