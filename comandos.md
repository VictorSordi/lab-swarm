docker swarm init --advertise-addr 192.168.56.2

docker swarm join --token <> 192.168.56.2:2377

docker swarm join --token SWMTKN-1-1d22j9uexbgcdg6ae8wcli7f3wi3zervv173sh16wxf8hqzjfi-ejw0ou6l3pdrriywdeueupm03 192.168.56.2:2377

docker node ls 

docker service create --name demo --publish 80:80 nginx

docker service scale demo=3