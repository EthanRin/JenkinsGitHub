pipeline{
    agent any

    stages{
        stage('Build'){
            steps{
                echo "Using Maven as the build automation tool"
                echo "Building and packaging..."
                
            }
        }
        stage('Unit and Integration Tests'){
            steps{
                echo "Using JUnit as the test automation tool"
                echo "Testing..."
            }
            post{
                success{
                    mail to: "sovanpanhaarinn@gmail.com"
                    subject: "Unit and Integration Tests Status Email"
                    body: "Test completed successfully!"
                }
                failure{
                    mail to: "sovanpanhaarinn@gmail.com"
                    subject: "Unit and Integration Tests Status Email"
                    body: "Test failed!"
                }
            }
        }
        stage('Code Analysis'){
            steps{
                echo "Using SOnarQube as the code analysis tool"
                echo "Analysing..."
            }
        }
        stage('Security Scan'){
            steps{
                echo "Using OWASP ZAP as the security scanner"
                echo "Scanning..."
            }
            post{
                success{
                    mail to: "sovanpanhaarinn@gmail.com"
                    subject: "Security Scan Status Email"
                    body: "Scan completed successfully!"
                }
                failure{
                    mail to: "sovanpanhaarinn@gmail.com"
                    subject: "Security Scan Status Email"
                    body: "Scan failed!"
                }
            }
        }
        stage('Deploy to Staging'){
            steps{
                echo "Using AWS EC2 as the staging server"
                echo "Deploying..."
            }
        }
        stage('Integration Tests on Staging'){
            steps{
                echo "Using JUnit to run integration tests on the staging server"
                echo "Testing..."
            }
            post{
                success{
                    mail to: "sovanpanhaarinn@gmail.com"
                    subject: "Staging Integration Tests Status Email"
                    body: "Test completed successfully!"
                }
                failure{
                    mail to: "sovanpanhaarinn@gmail.com"
                    subject: "Staging Integration Tests Status Email"
                    body: "Test failed!"
                }
            }
        }
        stage('Deploy to Production'){
            steps{
                echo "Using AWS EC2 as the production server"
                echo "Deployed!!!"
            }
        }
    }
}