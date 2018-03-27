node {
   // Mark the code checkout 'stage'....
   stage 'Checkout'

   // Checkout code from repository
   checkout scm
   sh 'printenv'
   sh 'path=`pwd` && pr_id=`echo $path | cut -d "-" -f2` && echo $pr_id'
   echo "set-build-description: bababababbaa"
   def currentBuild = Thread.currentThread().executable 
   def pattern = /^set-build-description: (.+)$/ 

   // Parsing 20 most recent lines of the build log 
   log = currentBuild.getLog(20) 
   for (line in log) { 
     match = (line =~ pattern) 
     if (match) { 
       currentBuild.setDescription(match[0][1]) 
       out.println "[set-build-description.groovy] Build description was set to: " + match[0][1] 
       break 
     } 
   } 
}
