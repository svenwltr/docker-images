zwm development environment
===========================

This image is for a private software project.

example fig.yml
---------------

	httpd:
		image: 'svenwltr/zwm-dev-env'
		links:
			- db:mongodb
		volumes:
			- app:/app
			- logs:/logs
		expose:
			- "80"
		environment:
			ZWM_DB_SERVER: 'mongodb://mongodb:27017'

	db:
		image: mongo
		command: mongod --smallfiles


