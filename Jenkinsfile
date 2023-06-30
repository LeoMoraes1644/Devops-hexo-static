pipeline {
    agent any

    environment {
        // Defina suas variáveis de ambiente, como a URL do seu repositório
        REPO_URL = 'https://github.com/LeoMoraes1644/Devops-hexo-static.git'
    }

    stages {

        stage('Setup') {
            steps {
                // Configurar o ambiente
                bat 'npx install'
            }
        }

        stage('Build') {
            steps {
                // Gerar arquivos estáticos com Hexo
                bat 'npx hexo generate'
            }
        }

        stage('Deploy') {
            steps {
                // Implementar com Hexo
                bat 'npx hexo deploy'
            }
        }

    }
}
