def gv
pipeline{
  agent any
  tools{
    maven 'maven'
  }
  stages{
    stage('init'){
      steps{
        script{
          gv = load "script.groovy"
        }
      }
    }
    stage('build jar'){
      steps{
        script{
          gv.buildJar()
        }
      }
    }
    stage('clear old images'){
      steps{
        script{
          gv.clearOldImages()
        }
      }
    }
    stage('build image'){
      steps{
         script{
             gv.buildImage()
         }
       }
    }
  }
}
