sudo chown -R botpress:botpress botpress/data botpress/language

docker-compose -f docker-compose-test.yaml up
docker-compose -f docker-compose-prod.yaml up

docker exec -it botpress/server /bin/bash

# Apply chmod 777 to all directories
sudo find botpress -type d -exec chmod 777 {} \;

# Apply chmod 777 to all files
sudo find botpress -type f -exec chmod 777 {} \;

# Apply chmod 777 to all directories
sudo find n8n_data -type d -exec chmod 777 {} \;

# Apply chmod 777 to all files
sudo find n8n_data -type f -exec chmod 777 {} \;

docker stop $(docker ps -aq)
docker rm $(docker ps -aq)
docker rmi $(docker images -q) 