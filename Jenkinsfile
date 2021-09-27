pipeline {
    agent any
    stages {
        stage('Setup parameters') {
            steps {
                script { 
                    properties([
                        parameters([
                            choice(
                                choices: ['ONE', 'TWO'], 
                                name: 'PARAMETER_01'
                            )
                        ])
                    ])
                }
            }
        }
        stage("Get Parameter") {
            steps {
                sh """
                echo $env.PARAMETER_01
                """
            }
        }
        stage("Deploy") {
            steps {
                sh """
                echo $env.Install_MTC
                """
            }
        }
    }
}
