docker swarm init --advertise-addr 192.168.56.2

docker swarm join --token <> 192.168.56.2:2377

docker node ls 

docker service create --name demo --publish 80:80 nginx

docker service scale demo=3

docker system prune