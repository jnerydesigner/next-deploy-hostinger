pipeline {
    agent any
    
    stages {
        stage('Node Search Curl') {            
            steps {
                script{
                    sh 'curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -'                
                }
            }
        }
        stage('Node Install Nodejs') {            
            steps {
                script{
                    sh 'sudo apt-get install -y nodejs'                
                }
            }
        }
        stage('Node Verifield') {            
            steps {
                script{
                    sh 'node -v'                
                }
            }
        }
        stage('Build') {            
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