# Kubernetes

kubectl get nodes
kubectl get pod

kubectlrun ngix --image <name>

kubectl delete pod <name>
kubectl apply -f filename 

kubectl logs -f pod-name nginx-
kubectl describe pod <name>

kubectl exec -it vote-5fc87bfc5f-sx6g8 bash
curl http://localhost:80

kubectl port-forward vote-5797468558-lz5nm 8080:80

curl localhost:8080

minikube ssh
ip addr show


kubectl expose pod vote-5797468558-lz5nm --type=LoadBalancer --name=vote-service

kubectl edit pod nginx<pod name>

kubectl get pod nginx -o yaml > second.yml
kubectl get redis -o yaml > second.yml-- in this case it will pick already created pod 

Ad hoc commands

kubectl run redis --image redis123
kubectl run my-deployment --image=nginx:latest --replicas=3


alias m='kubectl get po'

kubectl get pod -o wide


kubectl create deployment --name redis --image redis --replicas 3

Service commands 

kubectl describe service redis

#################################

version issues with python kubectl and awscli issues fix
sudo apt-get update 
1. sudo apt install python3-pip (Install Python3-Pip)
2. pip3 install awscli --upgrade --user (use Sudo if not run in the first place)
3. sudo rm /usr/local/bin/kubectl (removing the Kubectl)
4. https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/ (link to download Kubectl consists of 3 steps)
5. sudo apt install awscli (Before running aws eks update command check awscli version. If aws cLi is not present install it with the mentioned command)

Installing or updating eksctl
https://docs.aws.amazon.com/eks/latest/userguide/eksctl.html


#####################################
EKSCTL

https://docs.aws.amazon.com/eks/latest/userguide/eksctl.html

command-------------
eksctl create cluster -f cluster.yaml

eksctl delete cluster -f cluster.yaml

eksctl create ng -f filename

aws eks update-kubeconfig --region us-east-1 --name my-cluster
kubectl logs -f podname


-----------------------------------

namescpace 
 kubectl create ns qa
kubectl apply -f <filename> -n namespace


kubectl config use-context <contect-name>
kubectl config get-context 