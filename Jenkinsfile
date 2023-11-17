pipeline{
  agent{
     label{
        label "slave-1"
        customWorkspace "/mnt/slave1"
     }

  }

  stages{

      stage ("one")
      {
          steps{

            sh "sudo yum install httpd -y"
          }
         
      }
      stage("two")
      {
        steps {

             sh "sudo service httpd start"
             sh "sudo cp -r index.html /var/www/html/"
             sh "sudo chmod -R 777 /var/www/html/"
        }

      }
  }


}
