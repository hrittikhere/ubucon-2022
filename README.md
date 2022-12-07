## UbuCon 2022

### Build Image
docker build -t new:new .

docker run -d -p 5000:5000 new:new

### Start Kuberentes 
microk8s start


### Start cluster
microko8s kubectl get nodes

### Start Extension

microk8s enable dashboard

microk8s kubectl create token default

microk8s kubectl port-forward -n kube-system service/kubernetes-dashboard 10443:443

### Start Registry
microk8s enable registry


alias kubectl='microk8s kubectl'

### Push image
docker tag new:new localhost:32000/ubucon:latest

docker push localhost:32000/ubucon:latest

### Run Container
microk8s kubectl run test --image=localhost:32000/ubucon:latest

microk8s kubectl get pods

### Test Helm

microk8s helm

microk8s helm repo add bitnami https://charts.bitnami.com/bitnami

helm repo search nginx

### Test your image 

helm install 

helm repo remove bitnami

### Clean up

helm uninstall 