# Let's RUN with Ecommerce

## What to do
This assignment will help you familiarize with the micro service architecture based on Golang, 
Cobra and Docker along with the service structure, coding conventions and basic workflow. 
In this assignment, you are going to develop two services named **Company** and **Project** which perform 
Create, Read, Update, Delete and List action with a few calculation logic. 
These APIs will be exposed to both HTTP and GRPC client using Google Protocol Buffer.

### System architecture overview


### System database overview

  
### This assignment consists of 4 repositories
1. [Let's Run Docker](https://github.com/dinhtp/lets-run)
2. [Let's Run PbType](https://github.com/dinhtp/lets-run-pbtype)
3. [Customer Gateway Service](https://github.com/dinhtp/lets-run-customer)
4. [Platform Gateway Service](https://github.com/dinhtp/lets-run-platform)
5. [Shopify Customer Service](https://github.com/dinhtp/lets-run-shopify-customer)
6. [WooCommerce Customer Service](https://github.com/dinhtp/lets-run-woocommerce-customer)


##  Prerequisite
- Complete [Let's Go](https://github.com/dinhtp/lets-go) assignment


## How to use
### Docker command
In order to speed up the processing of spinning up the services with in the `docker-compose.yml` file, 
a few shell scripts created to quickly get the LAN IP, bring up and down the docker services. 
It is also required to take a look inside those scripts to understand the logic behind each command.

During the first run or everytime your local machine LAN IP is changed, it is required to execute the `./start`
command before bring up the docker services. Usually, this command is executed only once during each active session.

- Run `./start` to populate the LAN IP to docker environment.
- Run `./up` to bring up all the services in the docker compose file.
- Run `./down` to bring down all the services in the docker compose file.

### RUN Rest Service
Each Rest service written and built by Golang will carry a domain name defined in the `nginx.conf` file.
With each domain name, it is required to update the `hosts` file so that your local machine forward the request correctly.
For Linux users, the `hosts` file is located at `/etc/hosts`.
For Windows users, the `hosts` file is located at `C:\Windows\System32\drivers\etc\hosts`.

- Update the service domain name in the `hosts` file. For example: `127.0.0.1 api-go-company.local.com`
- To bring up all the services in the docker compose file, run `./up`
- Check if the service is up and running using `docker ps`

> NOTE: Changes in this repository ARE NOT REQUIRED to be committed into Github