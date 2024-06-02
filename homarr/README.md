Updating
To update, navigate to the directory with the docker-compose.yaml located.

Stop Homarr using docker compose down
Pull the newest image of Homarr using docker compose pull
Start Homarr again using docker compose up -d (-d for detached mode - start in background)
Delete the old image using docker image prune (Warning: this also removes you other unused images - not just Homarr)
You can automate this process using Watchtower.

Uninstalling
To uninstall, navigate to the directory with the docker-compose.yaml located.

Stop Homarr using docker compose down
Delete the created directories & files on your root file system (check docker-compose.yaml file for your specific locations)
Delete compose file using rm docker-compose.yaml
Prune unused Docker images using docker image prune (Warning: this also removes you other unused images - not just Homarr)
(Optional): Prune any network or volumes if you use any.
(Optional): Remove Homarr from your reverse proxy, VPNs or tunnels if you use any.






Docker will mount the configuration files and icons to your host machine. Please make sure to replace <your-path> from the docker run command with your desired storage location. The path must be absolute.

CAUTION
Make sure all your volumes path are pointing at different folders or the mounting will fail. Example of what NOT to do:

-v apps/homarr:/app/data/configs \
-v apps/homarr:/app/public/icons \
-v apps/homarr:/data

Instead do:

-v apps/homarr/configs:/app/data/configs \
-v apps/homarr/icons:/app/public/icons \
-v apps/homarr/data:/data

Updating
To update Homarr, you must remove your container first. Make sure that you've mounted your data and that you have access to it, so your configuration doesn't get lost.

Run docker rm homarr to remove the container.
Pull the latest Homarr image docker pull ghcr.io/ajnart/homarr:latest.
Re-run the command you used to install Homarr.
This process can get tideous, if you update frequently. Thus, we recommend the installation using docker-compose for more experienced users.

TIP
Want to update all your containers automatically? Checkout Watchtower a service which will automatically update your containers on a set interval.

Uninstalling
Obtain the container ID of your Homarr container using docker ps | grep homarr.
Delete the container using docker rm <your-container-id>
Prune unused Docker images using docker image prune (Warning: this also removes you other unused images - not just Homarr)
(Optional): Prune any network or volumes if you use any.
(Optional): Remove Homarr from your reverse proxy, VPNs or tunnels if you use any.