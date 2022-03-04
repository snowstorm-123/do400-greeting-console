pipeline{
    agent{
        label "nodejs"
    }
    stages{
        stage("Install dependencies"){
            steps{
                sh "npm ci"
            }
        }

        stage("Check Style"){
            steps{
                sh "npm run lint"
            }
        }

stage('Release') {

 steps {

 sh '''

 oc project maummv-greetings

 oc start-build greeting-console --follow --wait

 '''

 }

}

        stage("Test"){
            steps{
                sh "npm test"
            }
        }

        // Add the Release stage here
    }
}
