# Archean using docker compose

## Installing Docker

If you are running debian 11 or 12, the install docker bash file can be used to jumpstart your efforts.  Otherwise, check the install page for your system: https://docs.docker.com/engine/install/

## docker compose file

Store the `docker-compose.yml` in the same directory your `archean_data` directory is in.

### Running and managing the container

1. Pull the container with: `docker compose pull`
1. Start the container with: `docker compose up -d`
1. View the logs with: `docker compose logs archean --follow`
1. Halt the server with: `docker compose down`
1. Halt and remove the container: `docker compose stop && docker compose rm archean`

## Data directory

You should create a directory called `archean_data`, and in it you can store your config files, like `server.ini` or `admins.txt`

## Edit the server.ini

Edit the server.ini to your liking

| Parameter | Description |
|-----------|-------------|
| `[server]` | This section is for server details |
| `server_public_name` | Publicly visible server name (for the servers list) |
| `game_mode` | Select a game mode, 0: Creative, 1: Adventure |
| `server_online` | Do you want your server to be listed now? (yes/no) |
| `accept_remote_connections` | Do you want your server to accept remote connections? (yes/no) |
| `max_simultaneous_players` | How many players? 16 default |
| `password` | LEave empty for no password |
| `[networking]` | This section is for network related settings |
| `listen_port` | Listen port (default is 8881) |
| `listen_new_connection_timeout_ms` | new connection timeouts in milliseconds, 500 default |
| `automatic_blacklist` | default "no" |
| `[game]` | This section is for settings about the game and world |
| `world` | ... |
| `spawn` | Which entity to spawn on, by name.  earth default |
| `spawn_x` | Spawn X coordinate, default 2802212.000000 |
| `spawn_y` | Spawn Y coordinate, default -106687.000000 |
| `spawn_z` | Spawn Z coordinates, default -5532944.000000 |
| `updates_per_second` | default 25 |
| `physics_steps_per_update` | default 8 |
| `auto_save_interval_seconds` | default 30 |

## Edit the admins.txt

To add admins you only need the `steamID64` of each player.  You can see this in-game by hitting V (default) on a player.  You can also see it in the server logs when a player joins.  There are also websites you can use, if you know the steam profile URL, such as https://steamid.io

Your admins.txt should look something like this:

```
79956116265396957
79996196957162653
79996171626969553
```

