pipeline {
    agent any
    parameters{
        string 'JDK_VERSION'
        choice choices :['Dev','test','prod','stage'], name: 'Build_Environment' 
        password name: 'DB_Passward', defaultValue: 'welcome@9', description: 'defaultpassward'
        text name: 'DESC'
        booleanParam name: 'Deploy', description: 'Do whant to  deploy code on target env'
    }
    stages {
        stage('printparameters') {
            steps {
                echo "javaversion : ${parms.JDK_VERSION}"
                echo "Build environment: ${parms.Build_Environment}"
                echo "Db passward: ${parms.DB_Passward}"
                echo "Description: ${parms.DESC}"
                echo "Deploy : ${parms.Deploy}"
            }
        }
    }
}
