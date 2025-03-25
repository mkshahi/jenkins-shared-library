    @Library('test_library@main') _

pipeline {
    agent any
    parameters{
                string(name: 'ENV', defaultValue: 'dev', description: 'Target Environment')
                choice(name:'DEPLOY_TIME', choices:['full','partial'] )

    } 

    stages {
        
        stage('Hello') {
            steps {
                script{
                lib_module1.hello()
                if (params.ENV=="dev"){
                echo 'Hello World'
                }
                else{
                    echo "not dev"
                }
                }
                
            }
        }
    }
}
