pipeline {
  agent any

  triggers {
    GenericTrigger(
     genericVariables: [
       [key: 'name', value: '$actor.name']
    ],
    causeString: 'Triggered on $ref',
    token: 'test_token',
    tokenCredentialId: '',
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
