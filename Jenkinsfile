pipeline {
  agent any

  triggers {
    GenericTrigger(
     genericVariables: [
       [key: 'name', value: '$actor.name'],
       [key: 'reviewers', value: '$.pullRequest.reviewers'],
       [key: 'ref', value: '$.ref']
    ],
    causeString: 'Triggered on $ref',
    token: 'test_token',
    tokenCredentialId: '',
    printContributedVariables: true,
    printPostContent: true,
    silentResponse: false,
    regexpFilterText: '$ref',
    regexpFilterExpression: 'refs/heads/' + BRANCH_NAME
    )
  }

  stages {
    stage('Preparing') {
      steps {
        sh "echo Ref: $ref"
        sh "echo Name: $name"
        sh "echo Reviewers: $reviewers"
      }
