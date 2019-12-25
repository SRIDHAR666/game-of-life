node {
    
    stage('scm') {
    // some block
        git 'https://github.com/shaikkhajaibrahim/game-of-life.git'
    }
    
    stage('packaging') {
        sh 'mvn package'    
    }
    
    stage ('artifacts') {
        archiveArtifacts 'gameoflife-web/target/*.war'
    }
    
    stage ('junit') {
        junit 'gameoflife-web/target /surefire-reports/*.xml'
    }
}
