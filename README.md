# ansible_bootstrap_centos7_k8s_kind

Install Kind k8s using ansible

# Kind installation based on this article
https://www.linkedin.com/pulse/install-kind-kubernetes-cluster-linux-prayag-sangode/?trk=pulse-article_more-articles_related-content-card


# Install Ansible pre-bootstrapping
sudo yum -y update
sudo yum -y install epel-release ansible git

# Run playbook
ansible-pull -U https://github.com/markvtt/ansible_bootstrap_centos7_k8s_kind.git

# Post install
'''
[root@p5001 ~]# kind get clusters
k8s-playground

[root@p5001 ~]# kubectl cluster-info --context kind-k8s-playground 
Kubernetes control plane is running at https://127.0.0.1:44648
CoreDNS is running at https://127.0.0.1:44648/api/v1/namespaces/kube-system/services/kube-dns:dns/proxy
'''

# To create or delete cluster
kind create cluster --name k8s-playground --config kind-config.yml
kind delete cluster --name k8s-playground
