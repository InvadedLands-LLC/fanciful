pipeline {
    agent any
    tools {
        jdk '8'
    }
    stages {
        stage ('Build') {
            steps {
                withMaven(
                    mavenLocalRepo: '$WORKSPACE/.repository',
                ) {
                  sh "mvn clean deploy -DrepositoryId=invadedlands-repo"
                }
            }
        }
    }
}