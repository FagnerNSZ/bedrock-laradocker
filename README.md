# bedrock-laradocker
using bedrock and laradocker


------ RUM BERDROCK WORDPRESS IN LARADOCKER------

1 - In the past for aplication, in my case in bedrock 
	obs: your ladadocker folder will stay inside the bedrock folder so that the settings are applied to the Docker container in our case we will use the laradocker.
	
2 - Enter the folder and inside install the laradocker
	
3 -	git clone https://github.com/Laradock/laradock.git
 


Requeset for sintall Bedrock

PHP >= 5.6
Composer - Install

installation 

this comand install berdocke in diretory: 

4- Create a new project user composer php

 composer create-project roots/bedrock

5 -Copy .env.exemple to .env 
	DB_NAME - Database name
	DB_USER - Database user
	DB_PASSWORD - Database password

	DB_HOST - Database host
	WP_ENV - Set to environment (development, staging, production)
	WP_HOME - Full URL to WordPress home (http://example.com)
	WP_SITEURL - Full URL to WordPress including subdirectory (http://example.com/wp)
	AUTH_KEY, SECURE_AUTH_KEY, LOGGED_IN_KEY, NONCE_KEY, AUTH_SALT, SECURE_AUTH_SALT, LOGGED_IN_SALT, NONCE_SALT 	- Generate with wp-cli-dotenv-command or from the Roots WordPress Salt Generator
	Add theme(s) in web/app/themes as you would for a normal WordPress site.
	Set your site vhost document root to /path/to/site/web/ (/path/to/site/	comurrent/web/ if using deploys)
	Access WP admin at http://example.com/wp/wp-admin



---  .env in Bedrock --------------------------
	DB_NAME - Database name
	DB_USER - Database user
	DB_PASSWORD - Database password
	
	# Optional variables
	DB_HOST=mysql
	# DB_PREFIX=wp_

	WP_ENV=development
	WP_HOME=http://localhost/
	WP_SITEURL=${WP_HOME}/wp





6- intall laradock in diretory Bedrock

Clone Laradock inside your PHP project:

	url: http://laradock.io/
	git clone https://github.com/Laradock/laradock.git

7- configure the url aplication
	in nginx:  
	/repositorio_local/wp_berdock/bedrock/laradock/nginx/sites
	
8-	la no laradock goes to nginx in the default.conf file edit the root for location wordpress bedrock will be with this configuration


		root /var/www/public;

		edit for: 

		server_name localhost;
    	root /var/www/web;


9-	Then look for the mysqli flag inside laradock .env, and change to TRUE, because bedrock uses config acess databas.
	-------------------------------------------------
	this config rum laradocker:
	DB_NAME=databese name
	DB_USER=user database
	DB_PASSWORD= password database acess



