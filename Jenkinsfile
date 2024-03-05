pipeline {
    agent any
    
    stages {
        stage('Build') {            
            steps {
                script{
                    sh 'node -v'                
                }
            }
            steps {
                script{
                    sh 'npm run build'                
                }
            }
        }
        stage('Test') {
            steps {
                // Aqui você pode colocar comandos para executar testes
                sh 'echo "Executando testes..."'
            }
        }
        stage('Deploy') {
            steps {
                // Aqui você pode colocar comandos para implantar seu projeto
                sh 'echo "Implantando o projeto..."'
            }
        }
    }
    
    post {
        success {
            // Se a pipeline for bem-sucedida, você pode executar ações adicionais aqui
            echo 'Pipeline concluída com sucesso!'
        }
        failure {
            // Se a pipeline falhar, você pode executar ações adicionais aqui
            echo 'A pipeline falhou!'
        }
    }
}