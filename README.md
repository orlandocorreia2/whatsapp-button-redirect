Installation
git clone https://github.com/orlandocorreia2/whatsapp-button-redirect.git
Access application folder
cp .env.example .env
Setup docker database oracle
The database server is ready to use when the STATUS field shows (healthy) in the output of docker ps
The default password to connect to the database with sys user is Oradoc_db1.
Obs:. Give permissions to the volume folder if container qvc-db down and status exitted
docker exec -it qvc-db bash
sqlplus sys/Oradoc_db1@ORCLCDB as sysdba
alter session set "\_ORACLE_SCRIPT"=true;
create user root identified by root;
GRANT ALL PRIVILEGES TO root;
exit;
Setup Application
docker exec -it qvc-app bash
composer install
License
License

MIT license
ORLANDO CORREIA DO NASCIMENTO TECNOLOGIA DA INFORMAÇÃO 2020 © <a href="javascript:;" target="_blank">ORLANDO CORREIA DO NASCIMENTO TECNOLOGIA DA INFORMAÇÃO</a>.

## Installation

- `git clone https://github.com/orlandocorreia2/whatsapp-button-redirect.git`
- Copy folder whatsapp-button-redirect to your application folder
- In your page insert
- `<link rel="stylesheet" href="./whatsapp-button-redirect/dist/css/styles.css" />`
- `<script src="./whatsapp-button-redirect/dist/js/scripts.js"></script>`
- `<script> whatsBtnConfig = { ...whatsBtnConfig, phone: "5511948108855", path: "./whatsapp-button-redirect", logo: "https://orlandocorreia2.github.io/Site-Higienesp/assets/images/logo2-higienesp.png", companyName: "Higienesp", message: "Ola tudo bem", typingHint: "typing...", text: "Quero fazer um orcamento", }; </script>`

## License

[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)

- **[MIT license](https://mit-license.org/)**
- ORLANDO CORREIA DO NASCIMENTO TECNOLOGIA DA INFORMAÇÃO 2020 © <a href="javascript:;" target="_blank">ORLANDO CORREIA DO NASCIMENTO TECNOLOGIA DA INFORMAÇÃO</a>.
