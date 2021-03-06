## Run nginx Proxy

    cd ./
    docker-compose up -d
    
Then auto-restarts so is always up and running

## Commands

Start docker compose (run it)

    cd [project directory]
    docker-compose -d up

Stop docker compose (stop it)

    docker-compose down

Run composer update

    docker-compose exec app composer update
    
    # or
    
    alias cu="docker-compose exec app composer update"
    cu
    
Use NPM

    docker-compose run node bash
    npm install && npm run dev

or
    
    docker-compose run webpack sh -c 'npm install && npm run watch'
    
See logfiles

    docker-compose logs -f

## In your Laravel Project

Set this to get error logs from your docker container

    APP_LOG=errorlog
    
## Debugging

Use Port 9001

## Testing

A testing database will be created automatically

MYSQL_DATABASE = testing
MYSQL_USER = testing
MYSQL_PASSWORD = testing

Setup your remote php interpreter
- Languages & Frameworks > PHP > CLI Interpreter
- Choose "SSH Credentials". User "root". Auth Type "Key pair"
- If you do this the first time. Generate Public Key on your host. Copy your id_rsa.pub to authorized_hosts in your `~/.ssh` directory