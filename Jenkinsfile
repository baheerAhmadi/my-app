pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'Maven') {
				    echo "mvn clean complile"
                    mvn clean compile
					
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'Maven') {
				    echo "test stage"
                    mvn test
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'Maven') {
				    echo "maven deploy"
                    mvn deploy
                }
            }
        }
    }
}