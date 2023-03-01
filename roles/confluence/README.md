Write a markdown file with information

├── defaults
│   └── main.yml
├── handlers
│   └── main.yml
├── tasks
│   ├── config.yml
│   ├── main.yml
│   └── postgres.yml
├── templates
│   ├── conf
│   │   ├── confluence-init.properties.j2
│   │   ├── confluence.cfg.xml.j2
│   │   ├── server.xml-default.j2
│   │   └── server.xml.j2
│   ├── response.varfile.j2
│   └── systemd
│       └── confluence.service.j2
└── vars
    └── main.yml


- ```defaults``` folder: contains default variables for the role.
- ```vars``` folder: contains the other variables for the role.
- ```handlers``` folder: contains the handlers that will restart the postgresql service when the role is finished.
- Template folder contains template about confluence service, setup configuration for confluence
- In the task folder, the main.yml is to install confluence from deb package, the postgresql.yml is to create user and create database for confluence
Some variables you must know 
confluence_database_engine: postgresql
confluence_database_engine_version: 9.6
confluence_database_username: confluence
confluence_database_password: 123456
confluence_database_name: confluence
confluence_database_host: localhost
confluence_database_port: 5432