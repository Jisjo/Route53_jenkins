pipeline {
    agent any 
    
    stages {
        
        stage('Script initializing') {
            steps{
                git changelog: false, poll: false, url: 'https://github.com/Jisjo/Route53_jenkins.git'
            }}
        stage('Creating DNS Zone') {
            steps{
           sh label: '', script: '''cd ${WORKSPACE} ;
           pwd
           ls -l
           /bin/bash r53 ${domain_name} ${ip_address}
'''
            }
            
        }
            
        }
    }
