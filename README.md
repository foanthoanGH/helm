This is local repo for helm chart binary installation.


make helm user microk8s context
-
# Configuration
sudo mkdir /home/ubuntu/.kube
sudo chown ubuntu /home/ubuntu/.kube
microk8s config view > /home/ubuntu/.kube/config

#user one line:
sudo mkdir -p /home/ubuntu/.kube && sudo microk8s config view > /home/ubuntu/.kube/config && sudo chown -R ubuntu:ubuntu /home/ubuntu/.kube



# Installation
helm install monitoring ./kube-prometheus-stack/ --kube-context microk8s

go to the directory where you have the chart:

helm install <name> ./<chart name>

helm install mysql ./mysql ====ns will be mysql

# Uninstallation
helm uninstall monitoring ./kube-prometheus-stack/ --kube-context microk8s

# Upgrade (if needed)
helm upgrade monitoring --values=myvalues.yaml .



