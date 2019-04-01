* docker run --publish 3000:80 nginx
* port 3000 in your localhost will be forwarded to port 80 which is the port that nginx images use to wait for http connections.

* connecting application which run in docker container
* docker inspect <containerNameOrId>
* sudo docker inspect e85 | grep '"IPAddress"' | head -n 1
* docker inspect -f "{{ .NetworkSettings.IPAddress }}" <containerNameOrId>


#postgresql
sudo docker run --rm --name pg-docker -e POSTGRES_PASSWORD=q123123 -d -p 5432:5432 postgres

#pgadmin4
sudo docker run -p 8081:80 -e "PGADMIN_DEFAULT_EMAIL=elkhan.s.ibrahimov@gmail.com" -e "PGADMIN_DEFAULT_PASSWORD=q123123" -d dpage/pgadmin4

#rabbitmq
sudo docker run -d --hostname rabbit_host -v "rabbitmq_log:/home/elkhan/docker_container_data/rabbitmq/log" -v "rabbitmq_data:/home/elkhan/docker_container_data/rabbitmq/lib" -p 5672:5672 -p 5671:5671 -p 15672:15672 rabbitmq:3-management
sudo docker exec container_name_or_id ls -l /home/elkhan/docker_container_data/rabbitmq/log




