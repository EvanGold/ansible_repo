stage "checkout scm" {
checkout scm
}

stage "Ansible PlayBook"
{ 
    sh 'pwd; ls -l'
    sh('/etc/ansible/roles/geerlingguy.apache/bin/run_ansible')
}
