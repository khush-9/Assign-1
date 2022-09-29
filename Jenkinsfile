pipeline{
	agent {
	label {
		label 'slave2'
		customWorkspace '/slave2'
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
                                sh " sudo cp -r /slave2/index.html /var/www/html"
                                }
                        }
		}
	}

			
