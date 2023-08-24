---
title: "I love WINE; it hates me."
date: 2023-08-13 01:06:58 +0100
categories: [Music Production, Game Development]
tags: [music production, gamedev, linux, wine, mixcraft, gamemaker, godot]
author: <primedpixel>
---

[WINE](https://www.winehq.org/) is not an emulator, thus comes the acronym *"W.I.N.E."*, and is one of my favourite things. Why? Because I'm one of those cretins who had a mildly bad time with Windows, and then decided to sign away my rights and watch way too many [The Linux Experiment](https://www.youtube.com/c/TheLinuxExperiment) videos for my own good -- which is a long winded way of saying I began to use Linux. Honestly, the switch to Linux wasn't all too bad, and only two pieces of software were causing me trouble (i.e., had no equivalent that I initially planned on using).

WINE, via anything but emulation, allows Windows executables to run natively *(i think it counts as natively?)* on Linux. So, problem solved... right? Take any applications you used to run on Windows, and just shove 'em through the magic that is WINE?

## Game Development

![GameMaker: Studio 2 Logo](https://coal.gamemaker.io/sites/5d75794b3c84c70006700381/content_entry5f1ed2a9c4508d000782dcf3/5f5b8c56dbb16000072579be/files/gms2up.jpg?1678295770){: w="1920" h="1080"}
_The GameMaker: Studio 2 logo (now called, simply, "GameMaker")_

When I made the move to Linux, I still used [GameMaker](https://gamemaker.io/) (at the time called GameMaker: Studio 2) for creating games. It was the first game engine I properly put some time in, primarily through the likes of [Heartbeast](https://www.youtube.com/@uheartbeast) and [Shaun Spalding](https://www.youtube.com/@ShaunJS). But ever since the former began using it, a, now familiar, name began to pop up: **Godot**. I plan to talk about Godot in much more detail, but let's just say that it's *f\*cking fantastic* -- definitely a change from what I'm used to, and certainly something that I need to properly get stuck in to before I make something large scale, but brilliant nonetheless.

Godot became GameMaker's replacement. Sure, I tried running it through WINE, but alas to no avail. Then I tried an integrated virtual machine, but that's really clunky and definitely something that I wouldn't want to consistently use. Because of this -- and the fact that I needed to learn Godot for my A-Level programming project, because of [reasons that I implore you to read about](https://www.reddit.com/r/gamemaker/comments/rydlkz/rantish_cant_use_gamemaker_for_my_alevel_computer/) -- I stuck with using Godot, and I'm really quite glad with my decision. Plus, it's always good to get out of your comfort zone, and learn something new. There's no doubt that Godot has improved my ability to program simply due to it being different, requiring me to think differently about how to approach problems.

## Music Production
### REAPER
![Reaper DAW](https://www.reaper.fm/v6img/ss_persp_v63.jpg){: w="1000" h="450"}
_A screenshot of the DAW "Reaper", rotated on a 3D plane, or something like that, idk the technical term_

Okay... so why not use a DAW made specifically for Linux? I mean, I did the same for everything else (e.g., began using [GIMP](https://www.gimp.org/) instead of [paint.net](https://getpaint.net/)). Well, I tried [REAPER](https://www.reaper.fm/)... but VST support requires WINE anyway, and if I was to run the Windows version of REAPER through WINE anyway, I may as well stick with what I'm used to. That's not to say I will forever, to be fair. REAPER is certainly an extremely capable DAW, and probably much better than what I currently use, particularly for WINE compatibility. And you'll start to understand why shortly.

### Mixcraft

![Mixcraft DAW](/images/i-love-wine-it-hates-me/mixcraft-screenshot.png){: w="1920" h="1036"}
_A screenshot of an empty project inside Mixcraft, with the mixer panel open at the bottom_

Mixcraft is the name of the game. Specifically, Mixcraft 9: Recording Studio. Why 9? Well, it used to be the latest until version 10, very recently, came out. But I'm fine with 9, and got it all working on Linux... sort of.

WINE can be complicated to set up, particularly for a novice Linux user, such as myself. Many programs exist (particularly for gaming) to help with this, such as [Lutris](https://lutris.net/), or even [Steam](https://store.steampowered.com/) through [Proton](https://github.com/ValveSoftware/Proton), a custom version of WINE optimised for gaming. To help with my DAW troubles, however, I decided to use [Bottles](https://usebottles.com/). Bottles is a program that manages WINE prefixes (i.e., separate configurations of WINE, all running in different locations), and ensures a sandboxed environment, which can be useful a lot of the time. It *can* also be a bloody pain, but doesn't end up interrupting my workflow, really.

![Music Production Bottle in Bottles](/images/i-love-wine-it-hates-me/music-production-bottle.png){: w="1002" h="762" } So, after some initial set up, I managed to get Mixcraft working... in the Flatpak version of Bottles. Whilst this was actually a good thing, as Bottles encourages running through a Flatpak to ensure full sandboxing, it still baffles me that I could only get Mixcraft to work in this particular version, even if the runner is the same. What changes you ask? Well, for whatever reason, the non-Flatpak version of Bottles cannot use my audio device, thus I get absolutely no audio whatsoever -- which is kind of important if making music, I think.

Either way, when all is said and done, Mixcraft works quite well, and I've got VST support through WINE. Sure, there's been some hiccups, but overall nothing that 30 minutes on Google couldn't fix, such as the dreaded *Native Instruments VST install*. Although, ASIO is a pain in the backside that I just can't deal with right now -- if you need low latency for recording from something like a MIDI controller, be my guest and get [WineASIO](https://github.com/wineasio/wineasio) working, but for me, it's [more trouble than it's worth](https://www.reddit.com/r/winehq/comments/wmyj90/cant_make_wineasiodll/) *(mainly because [JACK](https://jackaudio.org/) is more trouble than it's worth)*

### Mouse Issues

So, why write all this down in a post on my website? Well, after needing to reinstall Linux for some reason I'm yet to fully understand *(something completely locked the file system, and made it impossible to boot, and also took up all the space on the drive?)*, and setting up the Bottle just fine, I began to run into a strange problem: the mouse sporadically froze. Seemingly at random intervals, but extremely often, my mouse would stop working. And even weirder, the light at the bottom of the mouse flashed whilst it was frozen, indicating it was disconnected. Surely enough, closing Mixcraft resolved this completely, and I had never encountered any other problems with the mouse on Linux. So, what the hell is up with that? Well, I'm not entirely sure what caused the issue, but I did manage to resolve it. I ended up changing three settings in Bottles to resolve this issue:

- Change "Synchronisation" under "Performance" to *"Esync"*
- Turn on *"LatencyFleX"* under "Components" (to the latest version available)
- Change the "Runner" under "Components" to *"GE Wine"*

Esync is likely to be the only thing that ended up mattering here, but I also think the other two generally improved performance in the Bottle. For those who don't know, [GE WINE](https://github.com/GloriousEggroll/wine-ge-custom) is a custom build of WINE based off of Steam's "Proton", but for use outside of Steam with non-steam games and applications. It's spectacular to have such a thriving community on Linux creating what are almost necessities for free, and keeping them open source. So, massive shout-out to [Glorious Eggroll](https://github.com/GloriousEggroll) for GE WINE, and all the [people who make WINE possible](https://wiki.winehq.org/Who's_Who) in the first place.

### Crashing

Even with that, WINE is not perfect, and I still get weird, and frankly annoying crashes in Mixcraft, from time to time. This is *not* an insult or criticism to the people who make WINE possible, however, but rather a warning to those who could -- and should -- use WINE. So, for the one person that sees this, please *for the love of all things holy*, do ***not*** press play and save in Mixcraft at the same time. You will corrupt your project file and have to use a backup, which is a minor inconvenience if you didn't save recently. Especially if you just cut up a bunch of takes playing the Casino Night Zone theme from Sonic 2.

![Casino Night Zone takes inside Mixcraft DAW](/images/i-love-wine-it-hates-me/casino-night-zone-takes.png){: w="704" h="168"}