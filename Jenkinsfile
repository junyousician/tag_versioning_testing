def set_up(){
  currentBuild.description = "bbb"
}
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
            sh 'echo bababababbaa > tmp'
            def port = readFile "tmp1"
            if (port?.trim()) {
              currentBuild.description = "${port}"
            } else {
              currentBuild.description = "no data"
            }

          }
        }
     }
   }


}
