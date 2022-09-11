# Minecraft Forge 1.7.10 (updated)

Hello there, fellow modders!
This repository is a fork of [Minecraft Forge](https://github.com/MinecraftForge/MinecraftForge) for Minecraft 1.7.10 containing various improvements and optimizations.
It is compatible with almost all mods out there (read more about incompatibilities at the end of the page) and is designed to improve the **user experience** and performance while keeping changes as small as possible. It is interchangeable with any other Forge 1.7.10 version, server and client.

## Improvements of this fork

Some of the most notable improvements of this fork include:
* A reduced startup time

## Goal of this fork
Originally, I intended to create a fork that removes the useless/broken Minecraft Realms and Mod Options... buttons to save space and improve the user experience, especially for new players.
However, I quickly came to realize that there are probably some more things that could be improved/adjusted without breaking mod compatibility, too.

Therefore, the goal is to create the **best 1.7.10 Forge version possible** that suits any mods/modpacks without creating any downsides/breaking anything that's even close to noteworthy, all of this while clearly stating every change made.

Note, however, that I do **not** intend to actively maintain/update this fork in general. I might make changes to it whenever I feel like it for whatever reason, but as Forge 1.7.10 is provenly stable, there will be no need to regularly update this fork.
**If you know something that could be improved (and is suitable for every/most use cases), don't hesitate to open an issue (or even PR) and tell me, though!**

## How well-tested is this fork/Can I safely use this?
I personally will use this fork anywhere I can, but I cannot guarantee that it won't break things and thus don't recommend to use this in any productive/important environment without deeply testing compatibility first.
Of course, **you're free to open issues if you encounter bugs and especially incompatibilities/crashes and PRs are always welcome, including new/updated language files**!

My **largest concern** about this fork is the fact that the building process for Forge 1.7.10 is somewhat broken (it errors and says "BUILD FAILED"). While it does generate a usable jar file, that jar file lacks some contents which are present in the latest official Forge 1.7.10 build.

## Building this fork
Setting up this fork for development works exactly the same way as with the official Forge 1.7.10.
Clone the repo to somewhere, run **gradlew setupForge eclipse** inside of it, then open Eclipse and select ./eclipse as workspace.

Building the fork is also identical to the official Forge 1.7.10: run **gradlew genPatches** (only required if working with/creating patches), then **gradlew build**. It will say "BUILD FAILED". However, upon entering ./build/distributions, you will find a working **forge-1.7.10...universal.jar** which you can use just like any other forge.jar.

## Incompatibilities
While this fork generally keeps up compatibility as much as possible, there are some niche cases where it might cause problems:
* BaseMods, which are fairly uncommon nowadays, are ignored/not loaded to allow for a notably quicker startup.
