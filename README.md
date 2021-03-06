# minecraft-luddite

[![Build Status](https://travis-ci.org/rremer/minecraft-luddite.svg?branch=master)](https://travis-ci.org/rremer/minecraft-luddite)

A Forge client/server modpack for Minecraft.

## Installation

Currently, this modpack is distributed as a [MultiMC] zip.

1. [Download MultiMC] and install.
2. Open MultiMC and and add login credentials
3. Click "Add Instance" and select "Import from zip" on the left-hand side.
4. Paste in this URL: [MMC client release 1.0.0] and hit <Enter> 
5. When the download finishes, double-click 'Luddite-1.0.0-client-mmc'
6. If you are not signed into a Mojang account, you will be promted for credentials

## Motivation

The drive behind this modpack's development was largely to make a more approachable world for new players, while coaxing veterans to explore different kinds of gameplay then they're used to.

Behaviors I found in my own gameplay (preferring modpacks with deep tech trees) which I specifically targetted for removal in this pack:
* exploration outside of your starting chunk is almost mandatory
* you won't need to go to the nether as soon as possible (in fact, I played many weeks without needing to go)
* you won't need to tech up to the best armor to feel safe
* you will be afraid of the night
* you are incentivised to farm (and not just find the most easily automatable food and eat that forever)
* multiplayer adventuring is not punishing (waiting for someone to pickup their grave), in fact death in general is less punishing

Issues and pull requests are welcome, and I encourage you to fork and enjoy!

## Development

This project is packed via a maven build:

```sh
mvn clean install
```

## Versioning

Versioning is semantic from the perspective of the client:

```MAJOR``` update must occur on client and server, and will invalidate existing worldgen.

```MINOR``` update must occur on client and server, existing worlds are compatible.

```PATCH``` update need only occur on the server.

## Server installation

Choose from the following pre-packaged releases:
 * [server release 1.0.0]

 You will find a ```start_server.sh``` script which will help you bootstrap the server. For self-provisioned cloud hosting, see [rremer/terraform-minecraft].


[MultiMC]:https://multimc.org/
[Download MultiMC]:https://multimc.org/#Download
[MMC client release 1.0.0]:https://storage.googleapis.com/minecraft-luddite/1.0.0/Luddite-1.0.0-client-mmc.zip
[server release 1.0.0]:https://storage.googleapis.com/minecraft-luddite/1.0.0/Luddite-1.0.0-server.zip
[rremer/terraform-minecraft]:https://github.com/rremer/terraform-minecraft
