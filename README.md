# Jenkins
pipline  {
     agent any
     satage {
         stage('clone repo and clean it') {
             steps {
                 sh "rm rf my-app"
                 sh "git clone https://github.com/workez12/almartha"
                 sh "mvn clean -f my-app"
             }
         }
         stage('test') {
             steps {
                 sh "mvn test -f my-app"
             }
         }
         stage('Deploy') {
             steps {
                 sh "mvn package -f my-app"
             }
         }
             }
         }
             }
         }
     }
}
