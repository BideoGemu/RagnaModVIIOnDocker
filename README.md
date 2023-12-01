# RagnaModVII on Docker

This repository was created for people who want to run MLDEG RagnaMod VII Modpack on a Docker based server.

Thanks to [itzg](https://github.com/itzg) for his work on itzg/docker-minecraft-server

To download the modpack go to [cursforge](https://legacy.curseforge.com/minecraft/modpacks/ragnamod-vii)

To run this server, it is imperative that docker-compose is installed.

How to install docker-compose: https://docs.docker.com/compose/install/

## How to do :

- Download or copy the docker-compose.yml file and place it on your server in the directory of your choice
- Download RagnaMod VII server files on curse forge and put in minecraft directory (with this docker-compose file, in directory: ./files) files and directory:
  * config/
  * defaultconfigs/
  * kubejs/
  * mods/
  * packmenu/
  * schematics/
  * eula.txt

Change eula config from false to true on eula.txt.

- run: `docker-compose up -d` in the directory where your docker-compose is located

## Environment option:

|Environnement Variable|Description|
|:--------------------:|:----:|
|OPS|Name(s) of the operator(s)|
|MEMORY| Memory allocated to server (Default: 10G) |
|ENFORCE_WHITELIST|"`TRUE` or `FALSE`"|
|TZ|Your time zone|

For more information on environment variables, do not hesitate to consult: https://github.com/itzg/docker-minecraft-server

You can also change the port exposed on your server by default, the port used is 25565. To modify it, simply replace the line `25565:25565` by `{external_access_port}:25565`

**Enjoy ! :)**
