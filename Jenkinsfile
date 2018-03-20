node {
    
    stage("checkout"){
        checkout scm
    }

    stage("Build"){

        withMaven(
            // Maven installation declared in the Jenkins "Global Tool Configuration"
            maven: 'M3',
            // Maven settings.xml file defined with the Jenkins Config File Provider Plugin
            // Maven settings and global settings can also be defined in Jenkins Global Tools Configuration
            mavenSettingsConfig: 'MyGlobalSettings',
            mavenLocalRepo: '.repository') {
     
          // Run the maven build
          sh "mvn clean install"
     
        }

    }
}
