This is local repo for helm chart binary installation.


make helm user microk8s context
-
microk8s config view
sudo mkdir /home/ubuntu/.kube
sudo chown ubuntu /home/ubuntu/.kube
microk8s config view > /home/ubuntu/.kube/config

To install:
-helm install monitoring ./kube-prometheus-stack/ --kube-context microk8s

To uninstall:

helm uninstall monitoring ./kube-prometheus-stack/ --kube-context microk8s



