pipelineJob ('seed job child private') {
  definition {
    cpsScm {
      lightweight()
      scm {
        git {
          branch ('main')
          remote {
            credentials('git')
            github('Anand1294/sample-repo3', 'ssh')
          }
        }
      }
      scriptPath('jenkinsfile')
    }
  }
  parameters {
    stringParam('argUrl', '', 'URL of the repository containing Jenkinsfile')
  }
  triggers {
    githubPush()
  }
}
