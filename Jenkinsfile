pipeline{
	agent{
		label{
			label  "slave-1"
		}
	}
	stages{
		stage("httpd install"){
			steps{
			sh "sudo yum install httpd -y"
			}
		}
		stage("httpd start"){
			steps{
				sh "sudo service httpd start"
			}
		}
		stage("index.html"){
			steps{
				sh "cp -r index.html /var/www/html/"
				sh "chmod -R 777 /var/www/html"
			}
		}
	}
}
