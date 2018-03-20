node {
    
    stage("checkout"){
        checkout scm
    }

    stage("Build"){

        withMaven(
            // Maven installation declared in the Jenkins "Global Tool Configuration"
            maven: 'maven',
            // Maven settings.xml file defined with the Jenkins Config File Provider Plugin
            // Maven settings and global settings can also be defined in Jenkins Global Tools Configuration
            mavenSettingsConfig: '5af0fc56-3fce-4a70-add1-6d39b7fdc2fd',
            mavenLocalRepo: '.repository') {
     
          // Run the maven build
          sh "mvn clean install"
     
        }

    }
}
