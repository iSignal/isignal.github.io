#Jenkins CLI notes
## Getting started with Jenkins CLI

## Set up authentication

The Jenkins command line tool needs to act as a Jenkins user to do its tasks, so it needs to authenticate. Authentication by manually typing in login and password is possible but discouraged. The easiest way is to use an ssh key pair to authenticate.

1. To learn how to generate an ssh key pair, follow these instructions. 
  1. [Digital Ocean guide] (https://www.digitalocean.com/community/tutorials/how-to-set-up-ssh-keys--2)
  1. `ssh-keygen -t rsa`
1. `cat .ssh/id_rsa.pub` and paste this into the SSH keys section at the jenkins user configuration page `http://ROOT_JENKINS/user/ADMIN_USER/configure`
1. Download the jenkins command line jar via `wget http://JENKINS_URL/jnlpJars/jenkins-cli.jar`
1. Now you can run `JENKINS_URL='http://ROOT_JENKINS/' java -jar jenkins-cli.jar help`

##

