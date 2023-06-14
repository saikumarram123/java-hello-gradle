pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    // Retrieve the username of the person who triggered the build
                    def triggerUser = env.CHANGE_AUTHOR
                    def cause = currentBuild.rawBuild.getCause(com.cloudbees.jenkins.plugins.GitHubPushCause)
                    
                    if (cause) {
                        triggerUser = cause.getTriggerSender().getDisplayName()
                    } else {
                        // Handle other trigger causes if needed
                    }
                    
                    // Print the username
                    echo "Build triggered by: ${triggerUser}"
                    
                    // Perform other build steps
                    // ...
                }
            }
        }
    }
}
