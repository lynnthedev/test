
pipeline {
      agent any
      stages {
          stage('21049462 Stage 1') {
            steps {
              sh 'echo "21049462 - Start of Pipeline"'
            }
          }
          stage('21049462 Stage 2') {
            steps {
              input("Push changes to Production?")
            }
          }
          stage('21049462 Stage 3') {
            when {
              not {
                branch "Push Changes to Production aborted"
              }
            }
            steps {
              sh '''#!/bin/bash
              bolt script run '/21049462/script_dir/21049462_script' -t websrv_21049462  -u clientadm -p user123 --no-host-key-check
              '''
              sh 'echo "Stage 3 Completed - 21049462'
            }
          }
          stage('21049462 Stage 4') {
            steps {
              sh 'echo "Production website tested working"'
                  
            }
          }
          stage('21049462 Stage 5') {
            steps {
              sh 'echo "Production website is updated successfully"'
            }
          }
      }
}
