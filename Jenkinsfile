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
