pipeline {
  agent any

  triggers {
    GenericTrigger(
     genericVariables: [
       [key: 'name', value: '$actor.name']
    ],
    printContributedVariables: true,
    printPostContent: true
    )
  }

  stages {
    stage('Preparing') {
      steps {
        sh "echo Name: $name"
      }
    }
  }
}
