# MySQL Playerdata Sync for Fabric/Paper

## Description
This is a server-side minecraft mod/plugin that allows players to sync their inventory(contains armor), enderchest inventory, and selected item slot between the server and another server.
This might be useful for a proxy based server(velocity, waterfall, bungeecord etc.)


## Installation
### Manual installation (recommended)
> **You have** to setup a **MySQL Database and MySQL User** for work with the database.
Download the latest version [Fabric](https://github.com/pugur523/MySQL_PlayerdataSync-4-Fabric/releases/latest)/[Paper](https://github.com/pugur523/MySQL_PlayerdataSync-4-Paper/releases/latest) then you can place the jar in the server's mods/plugins directory.
First time you reboot the server, you can find the config file in `config/playerdata_sync.conf` so stop the server and write your database url, user, and user password in the config file.(for more information about configuration, read configuration section below)
Then boot the server, setup is done.
On your login/logout, your playerdata should be loaded/saved from/to the database.

### Building from sources
Clone the repository(Fabric or Paper) and run `./gradlew build` then you can find the build artifacts in `build/libs`.

## Configuration
Fill in the configuration file which is `config/playerdata_sync.conf`.
There is 3 items named `jdbc.url`, `jdbc.user`, `jdbc.password` so set right side of them.


**Configuration Example**
```
jdbc.url=jdbc:mysql://localhost:80/example_database 
jdbc.user=example_user_name
jdbc.password=example_pass 
```

> for more information, join our [discord server](https://discord.gg/invite/xqfQMPEEZp)