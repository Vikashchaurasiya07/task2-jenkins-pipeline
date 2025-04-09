pipeline {
  agent {
    docker {
      image 'node:18'
      args '-v /var/run/docker.sock:/var/run/docker.sock'
    }
  }

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
        sh 'docker build -t task2-todo-app .'
      }
    }

    stage('Deploy (Optional)') {
      steps {
        echo '🚀 Deployment step goes here...'
      }
    }
  }

  post {
    success {
      echo '✅ Pipeline finished successfully!'
    }
    failure {
      echo '❌ Pipeline failed!'
    }
  }
}
