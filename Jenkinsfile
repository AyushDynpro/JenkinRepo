pipeline {
  agent any
  environment {
      MAJOR = '1'
      MINOR = '0'
  }
  stages {
    stage ('PostBuild') {
      steps {
        UiPathDeploy (
          packagePath: "path\\to\NuGetpackage",
          orchestratorAddress: "https://cloud.uipath.com/",
          orchestratorTenant: "DefaultTenant",
          folderName: "My Workspace",
          environments: "Dev",
          credentials: [$class: 'UserPassAuthenticationEntry', credentialsId: “credentialsId”],
          traceLoggingLevel: 'None'
        )
      }
    }
  }
}