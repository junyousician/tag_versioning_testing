pipeline {
    agent {
        node {
            label 'backend'
        }
    }
   // Mark the code checkout 'stage'....
   stage 'Checkout'
   checkout scm
   // Checkout code from repository
   stage 'test' {
     sh 'printenv'
     sh 'path=`pwd` && pr_id=`echo $path | cut -d "-" -f2` && echo $pr_id'
     echo "set-build-description: bababababbaa"
   }
   post {
     always {
       echo "post action"
     }
   }
}
