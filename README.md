# ansible_bootstrap_centos7_k8s_kind

# Install Ansible pre-bootstrapping
sudo yum -y update
sudo yum -y install epel-release ansible git

# Run playbook
ansible-pull -U https://github.com/markvtt/ansible_bootstrap_centos7_k8s_kind.git

# Kind installation based on this article
https://www.linkedin.com/pulse/install-kind-kubernetes-cluster-linux-prayag-sangode/?trk=pulse-article_more-articles_related-content-card
