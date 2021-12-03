Jenkins Pipelines
  Declarative workflow which is EASIER to Manage
  Workflow is TEXT document stored INSIDE git repository

Basic Pipeline system (Declarative)
pipeline {
  agent any
  stages {
    stage("Init"){
      steps{
        echo "This is INIT Stage"
      }
      
    }
    stage("Build"){
      steps{
        echo "This is BUILD Stage"
      }
      
    }
    stage("Deploy"){
      steps{
        echo "This is Deploy Stage"
      }
      
    }
  }
}


