node {
stage "checkout scm" {
checkout scm
}

stage "Ansible PlayBook" { 
    sh 'pwd; ls -al'
    sh('/etc/ansible/roles/geerlingguy.apache/bin/run_ansible')
}
}

