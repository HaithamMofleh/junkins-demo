pipeline {
    agent any
    parameters {
        string(name:'DEPLOY_VERSION' , defaultValue:'' , description:'')
        choice(name:'VERSION' , choices: ['1.0','1.2'] , description:'')
    }
    environment {
        NEW_VERSION ='1.0.0'
    }
    stages {
        stage("Build") {
            steps {
                echo "NEW_VERSION ${NEW_VERSION}"
                echo "VERSION ${params.VERSION}"
                echo "DEPLOY_VERSION ${params.DEPLOY_VERSION}"
            }
        }

        stage("Deploy") {
            when {
                expression {
                    BRANCH_NAME == 'dev'
                }
            }
            steps {
                echo "Deploy paras ${params.VERSION}"
            }
        }
    }
}
