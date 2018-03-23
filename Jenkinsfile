node {
   // Mark the code checkout 'stage'....
   stage 'Checkout'

   // Checkout code from repository
   checkout scm
   sh 'printenv'
   a = env.WORKSPACE
   echo "=========="
   pr_id = a.toString().tokenize( '-' )
   echo ${pr_id}
   echo ${pr_id[0]}
}
