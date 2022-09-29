pipeline {
	agent {
	label {
		label 'built-in'
		cutomWorkspace '/project'
		}
	}
          srtages {
		stage ('install-httpd') {
			steps {
				sh "yum install httpd -y"
				}
			}
		stage ('service start') {
                        steps {
                                sh "service httpd start"
                                }
                        }
		stage ('copy index') {
                        steps {
                                sh "cp -r /project/index.html /var/www/html"
                                }
                        }
		}
	}

			
