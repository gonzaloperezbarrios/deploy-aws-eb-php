# Deploy AWS EB

> Manual para realizar deploy utilizando AWS EB en un proyecto [Slim PHP](https://www.slimframework.com/)

## Pre-requisitos 

 - [Python](https://www.python.org/downloads/release/python-371/) 
 - [pip](https://pip.pypa.io/en/stable/installing/)

## Instalación 

    pip install awsebcli --upgrade --user
    aws --version
    eb --version
    
**Documentación de apoyo**
[AWS EB INSTALL](https://docs.aws.amazon.com/es_es/elasticbeanstalk/latest/dg/eb-cli3-install.html)

## Deploy

> Garantice que tenga las carpetas en la raíz del proyecto: 

 **.ebextensions** : Contiene los scripts que configura el contenedor elasticbeanstalk
  - 01_php-settings.config
  - 02_environment.config
  - 03_composer-install.config

 **.elasticbeanstalk** : Contiene el script que indica a que repositorio code commit y rama se debe conectar, y elasticbeanstalk que se le hace deploy
  - config.yml

> Ejecute los siguientes comandos en la raíz del proyecto en el shell 
 - eb init
 - eb status
 - [eb deploy --staged](https://docs.aws.amazon.com/es_es/elasticbeanstalk/latest/dg/eb-cli-codecommit.html) --debug

[Documentación comandos](https://docs.aws.amazon.com/es_es/elasticbeanstalk/latest/dg/eb-cli3-getting-started.html) 
