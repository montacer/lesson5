node('master'){
    
    stage("fetch source code"){
        git 'https://github.com/montacer/jenkins-github-ci-project'
    }
    
    dir('Lesson5'){
       
       printMessage('Running pipline')
       
       stage("Testing"){
           sh 'apk add python'
           sh 'python test_functions.py'
       }
       
       stage("development"){
           
           if(env.BRANCH_NAME == 'master'){
               
               printMessage('Deploying the master branch')
           
               
           } else {
               
               printMessage('NoDeployment configured for this branch')
           }
       }
       
       printMessage('Pipline Complete')
    }
}

def printMessage(message){
    echo "${message}"
}