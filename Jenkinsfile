pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'Maven') {
				    echo "mvn clean complile"
                    sh "mvn clean compile"
					
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'Maven') {
				    echo "test stage"
                    sh "mvn test"
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'Maven') {
				    echo "maven deploy"
                    sh "mvn deploy"
                }
            }
        }
    }
}