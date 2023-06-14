@Library('Slack')_
def sendSlackNotification(username) {
    // Set up Slack configuration
    def slackWebhookUrl = "https://hooks.slack.com/services/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"
    def slackChannel = "#mongo-testing"

    // Construct the Slack message
    def message = "Build triggered by: ${username}"

    // Send the Slack notification
    sh "curl -X POST -H 'Content-type: application/json' --data '{\"channel\":\"${slackChannel}\",\"text\":\"${message}\",\"username\":\"Jenkins\"}' ${slackWebhookUrl}"
}
