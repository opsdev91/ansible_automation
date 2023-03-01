Write a markdown file with information
This role is to install postgresql with 5 version 9.6, 10, 11, 12 ,13
├── README.md
├── defaults
│   └── main.yml
├── handlers
│   └── main.yml
├── tasks
│   ├── main.yml
│   ├── postgresql-9.6.yml
│   ├── postgresql-another-version.yml
│   └── variables.yml
└── vars
    └── main.yml

- ```defaults``` folder: contains default variables for the role.
- ```vars``` folder: contains the other variables for the role.
- ```handlers``` folder: contains the handlers that will restart the postgresql service when the role is finished.
-  main.yml file to direct to install version you want to install
- postgresql-9.6.yml to install postgresql-9.6 
- postgresql-another-version to install 4 version left

 variable you must define is postgresql_version 