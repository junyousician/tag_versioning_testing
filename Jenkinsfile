pipeline {
    agent {
        node {
            label 'backendBuild'
        }
    }
    stages {
     stage('stage1') {
       steps {
         script {
           sh 'printenv'
           sh 'path=`pwd` && pr_id=`echo $path | cut -d "-" -f2` && echo $pr_id'
         }
       }
     }

     stage('stage2') {
       steps {
         script {
            echo "set-build-description: bababababbaa"
            currentBuild.description = "aaa"
          }
        }
     }
   }


   post {
     always {
       steps {
         script {
            currentBuild.description = "bbb"
          }
       }
     }
   }
}
