# KESI-compose
Dokcer configuration for the KEIS system

# Description
The keis equipment managment system is quite difficult to set up correctly. To simplify the several step process, KEIS-compose is created
to help all wayward sons out there.

# Install
This guide will explain how to install KEIS on both x86 as well as arm based systems.

## Prequesities
 * Docker
 * Docker compose
 * Git

## Install
1. *Clone the repos and fetch submodules*
`git clone --recurse-submodules -j8 https://github.com/klyngen/KESI-compose`
2. *Set up the project*
If you wish to run this software on a normal linux machiene run the following
`docker-compose up`
For arm based architectures like the raspberry pi, I got you covered as well.
`docker-compose -f docker-compose-rpi.yml`
3. *Migrate the database*
 - Find the backend container by running `docker ps`
 - Enter the container by typing `docker exec -it <CONTAINER ID> php /var/www/artisan migrate`
4. *Enjoy*


## About the setup

### Backend
The backend uses Laravel and is served through nginx on port 5000. The backend should have been implemented in something more cloud firendly. Golang would be a better fit

### Frontend
The frontend is based on angular cli 6. Default is that the frontend listens on port 80

### Database
This build uses mysql, however it should really use mariadb. However, I am really a bigger fan of mariadb of pure principals
