node {
   // Mark the code checkout 'stage'....
   stage 'Checkout'

   // Checkout code from repository
   checkout scm
   sh 'printenv'
   sh 'path=`pwd` && pr_id=`echo $path | cut -d "-" -f2` && echo $pr_id'
   echo "set-build-description: bababababbaa"
}

post {
  always {
    echo "post action"
  }
}
