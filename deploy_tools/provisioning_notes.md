Provisioning a new site
=======================

## Required packages:

* nginx
* Python 3.6
* virtualenv + pip
* Git

eg, on Ubuntu:

    sudo add-apt-repository ppa:deadsnakes/ppa
    sudo apt update
    sudo apt install nginx git python3.6 python3.6-venv

## Nginx virtual Host config

* see nginx.template.conf
* replace DOMAN with, e.g., staging.my-domain.com

## Systemd service

* see gunicorn-systemd.template.service
* replate DOMAIN with, e.g., staging.my-domain.com

## Folder structure

Assume we have a user account at /home/username

/home/username
└── sites
    ├── DOMAIN1
    │   ├── .env
    │   ├── db.sqlite3
    │   ├── manage.py
    │   ├── static
    │   └── venv
    └── DOMAIN2
        ├── .env
        ├── db.sqlite3
        ├── etc
