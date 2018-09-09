# KESI-compose
Dokcer configuration for the KEIS system

# Description
The keis equipment managment system is quite difficult to set up correctly. To simplify the several step process, KEIS-compose is created
to help all wayward sons out there.

# Install

## Prequesities
 * Docker
 * Docker compose
 * Git

## Install
1. *Clone the repos and fetch submodules*
`git clone --recurse-submodules -j8 https://github.com/klyngen/KESI-compose`
2. *Set up the project*
`docker-compose up`
3. *Migrate the database*
 - Find the backend container by running `docker ps`
 - Enter the container by typing `docker exec -it <CONTAINER ID> php /var/www/artisan migrate`
4. *Enjoy*

