pipeline {
    agent { label 'ubuntu-agent' }
    stages {
        stage('Vérification du nœud') {
            steps {
                echo "✅ Job lancé sur : ${env.NODE_NAME}"
                sh 'hostname'
                sh 'uname -a'
                sh 'java -version'
            }
        }
        stage('Build') {
            steps {
                echo "🔨 Build en cours sur l'agent distant..."
                sh 'echo "Compilation simulée avec succès"'
            }
        }
        stage('Tests') {
            steps {
                echo "🧪 Lancement des tests..."
                sh 'echo "Test 1 : PASSED"'
                sh 'echo "Test 2 : PASSED"'
                sh 'echo "Tous les tests sont passés ✅"'
            }
        }
        stage('Déploiement') {
            steps {
                echo "🚀 Déploiement depuis l'agent distant..."
                sh 'echo "Application déployée avec succès"'
            }
        }
    }
    post {
        success {
            echo "✅ Pipeline terminé avec succès sur ubuntu-agent !"
        }
        failure {
            echo "❌ Échec du pipeline !"
        }
    }
} voila mon jenkinsfilee
