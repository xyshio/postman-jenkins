
pipeline{
    agent any
    environment {
        //M2_HOME = '/usr/local/Cellar/maven/3.5.4/libexec'
        //PATH = "$PATH:$M2_HOME/bin"
        DOCKER_HOME = '/usr/local'
        PATH = "$PATH:$DOCKER_HOME/bin"



    }
    stages {
        stage('Build'){
            steps{
                
                // sh 'mvn clean package'
                //sh "docker build . -t tomcatwebapp:${env.BUILD_ID}"
                sh 'newman run pmn.json --folder "Auth: Digest"'
                //sh 'docker image ls -a'
            }
        }
    }
}
