# Deploy_Ansible_AWX6_in_mins

above awx 3.0.0 envirments are no longer needed for awx_web and awx_task
replace by 3 files that need to be copy over from local into container. 

leave environment.sh SECRET_KEY credentials.py at the location of docker-compose.yml file

volumes:
      - "/root/SECRET_KEY:/etc/tower/SECRET_KEY"
      - "/root/environment.sh:/etc/tower/conf.d/environment.sh"
      - "/root/credentials.py:/etc/tower/conf.d/credentials.py"

docker-compose up -d 
should bring up the ansible_awx at port 80
