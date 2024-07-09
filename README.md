# docker-training


git clone https://github.com/venugopalsgnew/docker-training.git
ls
cd docker-training
cd Python-app/
ls
docker build -t python-app .
docker images
docker run -itd --name python-con10 python-app

docker ps                   -- Get the Container ID for the created container (python-con10)

docker exec -it e188e116426d /bin/bash               
curl localhost:5000
apt update -y
apt install curl -y
curl localhost:5000
We should be able to access "Hello world" Application 


------------------------------------------------------------
docker run -itd --name python-con11 -p 8070:5000 python-app

Enable Port 8070 at the security group of EC2 Instance

http://<Public_IP_EC2>:8070

We should be able to access "Hello world" Application 


