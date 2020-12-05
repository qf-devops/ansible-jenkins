node('ansible-label'){
  stage("git"){
   checkout scm
  }
  stage("ansible"){
   ansiblePlaybook disableHostKeyChecking: true, extras: 'group_name=jenkins', forks: 2, inventory: 'inventory.yml', playbook: 'jenkins.yml'
  }
}
