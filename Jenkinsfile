pipeline {
    agent {
        label 'qa'
    }
    
    stages {
        
        stage('Clean') {
            steps {
                sh 'mvn clean'
            }
        }
       
        
        stage('Build & Publish') {
            steps {
                sh 'mvn install package'
		       } 
        }
        stage('Save to tmp') {
            steps {
                sh 'mkdir -p /tmp/location_for_dashboard_artifacts; cd /tmp/location_for_dashboard_artifacts; cp *.jar /tmp/location_for_dashboard_artifacts'
            }        
        }
    }
}
