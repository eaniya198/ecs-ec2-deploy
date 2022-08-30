# ecs-ec2-deploy

#!/bin/bash
sudo amazon-linux-extras disable docker
sudo amazon-linux-extras install -y ecs
echo ECS_CLUSTER=test >> /etc/ecs/ecs.config;echo ECS_BACKEND_HOST= >> /etc/ecs/ecs.config;
systemctl restart ecs
systemctl enable ecs
