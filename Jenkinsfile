node{
    stage('Git Clone'){
        git 'https://github.com/mpratyu2208/calcwebapp.git'
    }
    stage('Maven Package'){
        def mvnHome = tool name: 'Maven', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    stage('Deployment'){ 
        sh 'cp target/*.war /opt/Tomcat/webapps'
    }    
}
