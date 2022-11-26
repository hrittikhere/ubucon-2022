## UbuCon 2022

microk8s start

microk8s enable dashboard

microk8s kubectl create token default

microk8s kubectl port-forward -n kube-system service/kubernetes-dashboard 10443:443

microk8s enable registry

docker build -t new:new .

docker run -d -p 5000:5000 new:new

docker tag new:new localhost:32000/ubucon:latest

docker push localhost:32000/ubucon:latest

microk8s kubectl run test --image=localhost:32000/ubucon:latest

microk8s kubectl get pods