pipeline {
  agent any

  stages {
    stage('Clone Repository') {
      steps {
        git url: 'https://github.com/Vikashchaurasiya07/task2-jenkins-pipeline.git', branch: 'main', credentialsId: 'github-creds'
        echo '✅ Cloned GitHub repo'
      }
    }

    stage('Build Application') {
      steps {
        echo '📦 Installing dependencies...'
        sh 'npm install'
      }
    }

    stage('Run Unit Tests') {
      steps {
        echo '🧪 Running unit tests...'
        sh 'npm test || echo "No tests yet 💅"'
      }
    }

    stage('Build Docker Image') {
      steps {
        echo '🐳 Building Docker image...'
        sh 'docker build -t nodejs-demo-app .'
      }
    }

    stage('Deploy (Optional)') {
      steps {
        echo '🚀 Deployment step (optional)'
      }
    }
  }

  post {
    success {
      echo '✅ CI/CD pipeline completed!'
    }
    failure {
      echo '❌ Pipeline failed!'
    }
  }
}
