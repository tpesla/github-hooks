pipeline {
    agent any

    stages {
        stage('Check PR Title') {
            steps {
                script {
                    // Replace this with the actual PR title from GitHub
                    String pullRequestTitle = "HYDRA-5555 | any_string | Name of PR"

                    boolean isValid = checkStructure(pullRequestTitle)

                    if (!isValid) {
                        error("Pull request title does not meet the required pattern.")
                    }
                }
            }
        }

        stage('Build') {
            steps {
                // Your build steps here
                echo 'Building...'
            }
        }

        stage('Test') {
            steps {
                // Your test steps here
                echo 'Testing...'
            }
        }
    }
}

boolean checkStructure(String s) {
    def pattern = /^[A-Za-z]+-\d{1,} \| .+ \| .+$/
    return (s ==~ pattern)
}      

