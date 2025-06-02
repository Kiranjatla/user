pipeline{

    agent any

    stages{
        stage('Code Quality'){
          steps{
              echo 'code quality'
              sh 'env'
              }
          }

        stage('Style Checks'){
           when{
           anyOf{
           branch 'main'
           tag "*"
           }
           }
          steps{
              echo 'Style Checks'
                    }
                    }
        stage('Unit Tests'){
        when{
          anyOf{
             branch 'main'
              tag "*"
             }
               }
          steps{
              echo 'Unit Tests'
                    }
                }
        stage('Download Dependencies'){
          when{ tag "*" }
          steps{
              echo 'Download Dependencies'
                    }
                }
        stage('Prepare Artifact'){
           when{ tag "*" }
           steps{
               echo 'Prepare Artifact'
                    }
                }
       stage('Publish Artifact'){
           when{ tag "*" }
                         steps{
                             echo 'Publish Artifact'
                    }
                }
       }

     }
