# AMOS
Rethinking addon distribution.

## The current situation in Arma 3

Currently distributing and downloading mods is a very tedious process.
There are some pages like [Armaholic](http://www.armaholic.com/) that also function as distribution hubs.

### As the addon creator
You have to build your addon with whatever tools you prefer and then distribute it as a zip file. 
Either on your private webspace or on filehosters.

The packaging for these zip files is not standardized. So for every new addon you have to figure out how to do it in the 
best possible way.

### As the addon manager for a community
You have to know where to get the addons from. You have to know all the different websites and other distribution channels. You have
to have the state of every addon in your head (or a spreadsheet).

Once patchday hits you have to visit every single site, check for new versions, download them manually and then distribute it to your server.
Then (depending on the tool you use) you have to update the distribution mechanism of your choice and hope that everything "just works".

### As the community member
You have to get used to more or less complex and confusing tools that will help you (or stand in your way) to get all the addons that you need for a gameday.


## The plan with AMOS

AMOS is aimed at solving these problems by providing an integrated toolset from start to finish.

!Important!: This does **NOT** mean any fancy UI. `AMOS` will (in the beginning) just provide simple tools and libraries that other tool creators
(like A3S or PlayWithSix) can build on to ease addon distribution for them.

The plan is that in the future the process looks like this:

### As the addon creator

You use a tool based on `AMOS` to pack your addon in a standard way.
Then you use `AMOS` to push the newest version of your addon to a remote distribution hub (this can be your own or some larger, 
more centralized one).

### As the addon manager for a community

You use `AMOS` to get a list of all available updates for all addons you have installed.
You select the addons you want to upgrade from said list and then `AMOS` will do the downloading, verification and unpacking for you and also
provide you with a shortcut to start your server.

### As the coomunity member
You can use `AMOS` to get the latest version of all addons as specified on the server you want to play on.

## But.. Why?

The process is taken from [Maven](https://maven.apache.org/) or basically every other `Dependency Management` tool known in Software engineering today.
The interesting aspect of this is that it removes the need for manual tracking and downloading of dependencies (addons, libs) for all involved parties.

This specifically also enables some interesting use cases.
Lets say you are developing a weapon pack like [RHS](http://www.rhsmods.org/). You can distribute it as a huge group of items and thus force
everyone to use all of it.

With the `AMOS` system you could provide every single gun as its own addon and then also provide a grouped addon set ("RHS ALL Weapons") as a convenience.
Of course this also works for other dependencies. E.g. some Weapons depend on files created for other guns (if I remember correctly some RHS assault rifles all depend
on the same M4 config file). With the `AMOS` system you could distribute said dependency (the config file) as a single artifact. Then all your
other guns can have a dependency on it and will be available for your users when they want to use your gun.

With this the whole addon system becomes much more flexible and we remove one important step.
Currenlty some communities are manually packing parts of Addons into their own, custom groups. Some also rename files (make everything lowercase).
This makes it virtually impossible to synchronize addon sets over multiple communities. `AMOS` tries to fix this by providing an easy, integrated
approach to addon distribution and dependency management.

## Current State
Currently this is a theoretical draft. As soon as there is enough interest in the community I would start working on this and also invite everyone interested
to help out. Until then feel free to create issues with new ideas or pull request with changes for this document.


## License
The MIT License (MIT)

Copyright (c) 2016 Jonas

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
