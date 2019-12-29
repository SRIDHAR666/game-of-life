pipeline {
    agent any
    stages {
        stage ('Git') {
            steps {
                git 'https://github.com/venkychowdary/game-of-life.git' branch ''
            }   
        }
        stage ('package') {
            steps {
                sh 'mvn package'
            }
        }
        stage ('Artifact') {
            steps {
                archiveArtifacts 'gameoflife-web/target/*.war'
            }
        }
        stage ('Junit') {
            steps {
                junit 'gameoflife-web/target/surefire-reports/*.xml'
            }  
        }
        stage ('Sucess') {
            steps {
                echo 'Congratulations Venky Chowdary Bommgani Build is Sucess'
            }
        }
    }
}
