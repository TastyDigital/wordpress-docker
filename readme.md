# Wordpress Docker Development Environment

## Clone this repo and install dependencies

Install PHP plugin dependencies: `composer install`

You may need to setup SSH Key access to install plugins from private repositories.

## Docker Compose 

Install Docker Desktop, and disable any other MySQL databases or webservers (such as MAMP) to prevent a service conflict (this always catches me out).

Then fire up the containers (Wordpress and MySQL): 
`docker-compose up`

It can take a minute for the containers to start the first time. When they have started, open a web browser and go to [`localhost`](http://localhost) to start your website and install WordPress. You can stop the containers by pressing `Ctrl-c` inside of the terminal window in which you started the containers.
 
## Login to Wordpress

Install new Wordpress, creating account and [login](http://localhost/wp-login.php). Activate development plugins, including JWT Auth Web tokens.

For Javascript Web Tokens, get your bearer token by posting valid username and password login credentials as form data to http://localhost/wp-json/jwt-auth/v1/token.