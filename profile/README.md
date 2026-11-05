<div align="center">

# ngspades

**The ngspades protocol for Ace of Spades, alive again, and Shoot and Destroy,
its reference client and server.**

[![Website](https://img.shields.io/badge/website-shootanddestroy.obex.pw-2ea44f?style=for-the-badge)](https://shootanddestroy.obex.pw)
[![Protocol](https://img.shields.io/badge/protocol-docs-orange?style=for-the-badge)](https://github.com/ngspades/protocol)
[![X](https://img.shields.io/badge/follow-%40itxtoledo-000000?style=for-the-badge&logo=x)](https://x.com/itxtoledo)
[![License](https://img.shields.io/badge/license-GPLv3-blue?style=for-the-badge)](https://www.gnu.org/licenses/gpl-3.0)

</div>

---

## Where the name comes from

**ngspades** was a branch of [OpenSpades](https://github.com/yvt/openspades), the
open source Ace of Spades client written by [yvt](https://github.com/yvt) and its
contributors. Between 2013 and 2014 that branch designed a new network protocol
for Ace of Spades (its wire calls itself `WorldOfSpades`), meant to replace the
0.75 protocol every public server still speaks: entities and trajectories instead
of fixed packets, a proper handshake with versions and certificates. The branch was
left as a prototype. Its codec was complete, its game was not.

We picked it up where it stopped. Our **protocol 1.0** starts from the ngspades
wire format, fixes its defects and adds what a whole game needs (building, digging,
chat, game modes, classes, perks, bots). It is documented, packet by packet, in
[ngspades/protocol](https://github.com/ngspades/protocol), together with 0.75 and
0.76, so anyone can write a client or a server that plays with ours.

This organization is named after that work as a credit to it. It is not the
OpenSpades project and is not run by its authors; the original ngspades code is
theirs, under its own licence, in the
[OpenSpades repository](https://github.com/yvt/openspades).

## Shoot and Destroy, the reference client and server

**Shoot and Destroy** is the game that implements the ngspades protocol, and the
reference for it: one client that speaks protocol 1.0 with our servers and keeps
joining every public 0.75 / 0.76 server, and a server that speaks 1.0 (or, in its
classic profile, 0.75).

- **Singleplayer that is a real server.** Starting a match runs the dedicated server
  locally and joins it: offline and online are the same game, and friends can join you.
- **Bots that play like people.** They plan their way to the objective (digging,
  bridging, swimming out), take cover, hear digging, and split CTF into roles:
  defenders, infiltrators tunnelling with a bodyguard, snipers, rushers.
- **Classes and perks.** Commando, Rocketeer, Marksman and Miner, each with its own
  gear and streak perk: sentry guns, landmines, dynamite, revives, jetpacks.
- **Many modes.** Classic and next gen CTF, Babel, Arena, Zombies, King of the Hill,
  Territory Control, Creative, and Lua game modes from plugins.
- **Up to 128 players a match**, bots included.
- **Gamepad first.** Every menu and every action works with a controller, for
  handhelds and consoles.
- **Everywhere.** Linux, macOS, Windows, iOS, Android, the browser and handhelds.

## Make it yours

| Repository | What is in it |
| --- | --- |
| 📡 **[protocol](https://github.com/ngspades/protocol)** | The protocols, documented for implementers: ngspades 1.0, Ace of Spades 0.75 / 0.76 and its extensions, the master server and the ping queries, with C and Godot examples. |
| 🗺️ **[maps](https://github.com/ngspades/maps)** | Every Ace of Spades map from [aos.party](https://aos.party) (891 of them), with the original pyspades `.txt` and a `.toml` ready for a Shoot and Destroy server. Copy a folder, add it to your rotation. |
| 🧩 **[plugins](https://github.com/ngspades/plugins)** | Lua plugins for Shoot and Destroy servers: game modes, mechanics, admin and building tools, most of them pyspades / PySnip scripts ported to Lua. Includes the plugin API and examples to write your own. |

## Credits

Shoot and Destroy stands on the shoulders of the Ace of Spades community:
protocol 1.0 starts from the ngspades branch of
[OpenSpades](https://github.com/yvt/openspades) by yvt and its contributors, the
client is a fork of [ButterSpades](https://butter.penguins.win) (itself a fork of
[BetterSpades](https://github.com/xtreme8000/BetterSpades)), and the server a fork of
[SpadesX](https://github.com/SpadesX/SpadesX). Thank you to every map maker and
script author whose work lives on here.
