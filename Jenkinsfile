Jenkinsfile (Declarative Pipeline)
pipeline {
    agent any

    stages {
        stage('playbook') {
            steps {
                sh 'ssh -i /var/jenkins_home/job.pem centos@172.17.0.1 "cd /var/ansible/ansible_repo && git pull" '
                sh 'ssh -i /var/jenkins_home/job.pem centos@172.17.0.1 "/etc/ansible/roles/geerlingguy.apache/bin/run_ansible"'
            }
        }
    }
}

ssh -i /var/jenkins_home/job.pem centos@172.17.0.1 'sudo sh -c "cd /var/tmp/ansible_repo; pwd; git pull" '

ssh -i /var/jenkins_home/job.pem centos@172.17.0.1 'sudo rsync -av /var/tmp/ansible_repo/ /etc/ansible/'

ssh -i /var/jenkins_home/job.pem centos@172.17.0.1 'sudo /root/terraform/up'

ssh -i /var/jenkins_home/job.pem centos@172.17.0.1 'sudo /etc/ansible/roles/geerlingguy.apache/bin/run_ansible'

#ssh -i /var/jenkins_home/job.pem centos@172.17.0.1 'sudo /root/terraform/down'
