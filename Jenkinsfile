pipeline{
	agent {
	label {
		label 'slave1'
		customWorkspace '/slave1'
		}
	}
          stages {
		stage ('install-httpd') {
			steps {
				sh "sudo yum install httpd -y"
				}
			}
		stage ('service start') {
                        steps {
                                sh "sudo service httpd start"
                                }
                        }
		stage ('copy index') {
                        steps {
                                sh " sudo cp -r /slave1/index.html /var/www/html"
                                }
                        }
		}
	}

			
