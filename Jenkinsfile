pipeline {
    agent {
        node {
            label 'backend'
        }
    }
    stages {
     stage('stage1') {
       sh 'printenv'
       sh 'path=`pwd` && pr_id=`echo $path | cut -d "-" -f2` && echo $pr_id'
     }

     stage('stage2') {
       echo "set-build-description: bababababbaa"
     }
   }


   post {
     always {
       echo "post action"
     }
   }
}
