
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building Calculator'
            }
        }

        stage('Test Addition') {
            steps {
                script {
                    def a = 10
                    def b = 20
                    def result = a + b

                    echo "Addition: ${a} + ${b} = ${result}"

                    if (result == 30) {
                        echo 'Addition Test Passed'
                    } else {
                        error 'Addition Test Failed'
                    }
                }
            }
        }

        stage('Test Multiplication') {
            steps {
                script {
                    def result = 5 * 4
                    echo "Multiplication: 5 * 4 = ${result}"

                    if (result == 20) {
                        echo 'Multiplication Test Passed'
                    } else {
                        error 'Multiplication Test Failed'
                    }
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Calculator is ready!'
            }
        }
    }

    post {
        success {
            echo 'CI Pipeline completed successfully!'
        }
        failure {
            echo 'CI Pipeline failed!'
        }
    }
}
