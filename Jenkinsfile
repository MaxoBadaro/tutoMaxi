pipeline {
    agent { label 'tuto' }
    

    stages {
        stage('Build') {
            steps {
                container('flyway') {
                    script {
                        sh 'flyway info -url="jdbc:mysql://mysql.mysql.svc.cluster.local:3306/devops" -user=root -password=devop2022'
                        sh 'flyway migrate -locations=filesystem:scripts -url="jdbc:mysql://mysql.mysql.svc.cluster.local:3306/devops" -user=root -password=devop2022'
                        sh 'flyway info -url="jdbc:mysql://mysql.mysql.svc.cluster.local:3306/devops" -user=elon -password=musk'
                    }
                }
            }
        }
    }
}
