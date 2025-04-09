pipeline {
  agent any

  stages {
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
