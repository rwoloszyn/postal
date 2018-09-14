1. Clone the Postal git repository and place the files from this gist in the root folder.
1. `docker-compose build`
1. `docker-compose up -d mysql`
1. `docker-compose run web bin/postal initialize-config`
1. `docker run -it -v postal_config:/opt/postal/config alpine vi /opt/postal/config/postal.yml`
1. See the attached `postal.yml` for the correct `message_db`, `main_db`, and `rabbitmq` settings and make the necessary edits.
1. `docker-compose run web bin/postal initialize`
1. `docker-compose up`

App should be running at http://<your_docker_host_ip>:5000/.