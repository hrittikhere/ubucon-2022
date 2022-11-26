## UbuCon 2022

docker build -t new:new .

docker run -d -p 7111:3111 new:new

docker tag nginx:latest localhost:32000/mynginx:latest

docker push localhost:32000/mynginx:latest

microk8s kubectl run test --image=localhost:32000/mynginx:latest

