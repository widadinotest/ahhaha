pipeline {
    agent any
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
                echo "🔨 Build en cours..."
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
                echo "🚀 Déploiement..."
                sh 'echo "Application déployée avec succès"'
            }
        }
    }
    post {
        success {
            echo "✅ Pipeline terminé avec succès !"
        }
        failure {
            echo "❌ Échec du pipeline !"
        }
    }
}
