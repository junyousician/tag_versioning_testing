node {
   // Mark the code checkout 'stage'....
   stage 'Checkout'

   // Checkout code from repository
   checkout scm
   sh 'printenv'
   a = env.WORKSPACE
   echo "=========="
   echo a
}
