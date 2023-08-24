---
title: "Lessons I've Learnt From Celeste's Level Design"
date: 2023-08-24 19:43:38 +0100
categories: [Game Development, Level Design]
tags: [gamedev, level design, xekino, godot, platformers, celeste]
author: <primedpixel>
---

![Celeste Artwork](https://images.igdb.com/igdb/image/upload/t_original/ar7u5.jpg){: w="689" h="388"}
_Artwork of Celeste, featuring the main protagonist "Madeline", main antagonist, affectionately known as "Badeline", and "Theo"_

Celeste is one of my favourite games of all time, which is why I obsess over emulating what makes it succeed in my own games -- XΞKINO is a platformer, currently very early in development, and as with all platformers, I need to think about how to make it actually fun, i.e., level design. So, I ask myself, why not take a look at one of the greatest platformers -- nay, greatest games -- of all time.

Lead developer of Celeste, [Maddy Thorson](https://mastodon.gamedev.place/@maddy), or [Maddy Makes Games](https://www.maddymakesgames.com/) spoke in depth about her approach to designing Celeste at the [2017 Game Developer's Conference](https://www.youtube.com/watch?v=4RlpMhBKNr0), which is effectively my entire reference for this post.

## Areas and Levels
Celeste is split up into two sub-sections: *areas*, or chapters, and *levels*. Levels in Celeste are miniscule problems the player has to solve. These small sections of platforming challenge ultimately make up the entirety of one area, which then makes up the game. It's important for levels to be appropriately varied, as well as tie into the overall area, and therefore game. Without enough variety, levels can feel stale, yet too much can give the player whiplash, and be confusing. As with many things, the golden mean is key.

Whilst "level design" is a buzzword often thrown around for how well the game is "put together", so to speak, I'm going to particularly focus on what Celeste calls levels, their design, and why I think this is a brilliant way of platformer design. An analysis of Celeste's area design will probably come at a later date.

## Story Based Level Design
![Screenshot of Celeste](https://images.igdb.com/igdb/image/upload/t_original/fkbchtayhzmfnljfusel.jpg){: w="689" h="388"}
_Screenshot of Celeste, featuring dialogue with an NPC -- you'd think this is the story i'm on about, but that's not the case_

Celeste's main intention is to design levels around a **story** -- that is, not just be a series of particular inputs the player has to make. So, how is a level split into a story? Effectively, levels need to have a minimum of:
- Beginning -- the opportunity for the player to scope out the level and key details within it
- Tension -- some initial problem for the player to solve
- Climax -- some final, generally more difficult problem, for the player to solve
- Resolution -- a reward for the player, which can be as simple as level progression, or a collectible

Levels may require additional layers of story, and this structure is not strict -- *in fact, it's something I've entirely made up, but based off of Celeste and its levels* -- but it serves as a general guideline for designing levels with a story in mind. It's important not to over-complicate the story. A question that should be constantly asked is: "should this be where the level ends?". Ensure that each story has variety, as to not feel monotonous, and ensure that levels are digestible, and not overwhelming.

Certain parts of the level should be highlighted by the level design, in order to tell the intended story.

> The player should remember the story of the level, and not the series of inputs required to complete said level.
{: .prompt-info}

## Designing Levels Around Problem Solving
![Screenshot of Celeste](https://images.igdb.com/igdb/image/upload/t_original/rougracf4aao1ebhxxy9.jpg){: w="690" h="388"}
_Screenshot of Celeste, featuring a level near the beginning of the game, with three platforms on the ground, one in the air, and one that will fall_

Levels in Celeste are made akin to a rock-climbing wall, in that there are a multitude of different ways to complete one obvious goal. Even the simplest of problems, e.g., crossing a small gap with one platform in the middle, should have multiple ways to be solved. In Celeste's case, this could be the option to dash over the central platform, or jump on each platform individually. Obviously, more complicated levels inherently lend themselves to more variety in level solutions, but it should always be a central focus to ensure different ways of completion.

> Different players have different play-styles; all should be accommodated, but also challenged.
{: .prompt-info}

Players should be able to "read" the level easily, i.e., understand the main *intended solutions* -- however, there should not be only one singular solution that the player must follow. Thus, things that are definitely not intended should be highlighted to be such -- make impossible things impossible, in order to not have the player hyper-fixate on an, initially, seemingly difficult but possible manoeuvre.

However, once a level is fully designed, it can be beneficial to add, obviously "non-intended" (i.e., not meant to be a part of the standard set of solutions), but possible, difficult ways to solve the problem. This is to reward the experienced player for their skill, and to provide an alternative story for the level.

> It's crucial that no-one mistakes this as an intended path. These more difficult additions should only come once the level design is 110% finalised.
{: .prompt-warning}

## Designing Levels Around Safety
![Screenshot of Celeste](https://images.igdb.com/igdb/image/upload/t_original/zr67hixr4lsfbtg9rlwk.jpg){: w="689" h="388"}
_Screenshot of Celeste, featuring a level near the end of the main game_

In order for the story of the level to be well-paced, the **safety** during the progression of a level needs to be considered. Here, safety is being defined as how long the player can stay still before being killed, or otherwise failing to solve the problem of the level. So, a generic platform on the ground is considered very safe, whereas a platform that crumbles away after 5 seconds is considered mildly unsafe, and holding onto a ledge without any "grip-strength" is considered extremely unsafe.

The length of a level works in tandem with its safety; a longer level results in more progress lost when failed, thus making the safety lessen as the level progresses. High stakes with long levels amplify the perceived difficulty of the level.

## Why This Works
It's difficult to understand, and articulate, why this method of level-design works so well. It's important to recognise that, due to Celeste's overall structure, over-arching story, and narrative style, it's likely that the "story" methodology generally lends itself to work well. However, even disregarding Celeste, this level-design philosophy provides some important features:
- Levels are made for everyone, making the game feel more approachable, but not annoyingly easy. Ensuring that there are multiple ways to go about solving a level is a sure-fire way to create a game that can have difficulty without feeling frustrating. Never in Celeste does it feel unfair, and this is because the levels are effectively designed for every type of player (or as much as they reasonably can be). This is why play-testing in a platformer game is so, so essential -- you need that wide variety of players to provide feedback often.
- Levels are varied, unique, and memorable. Particularly when considering safety, it's easy to see how thinking about levels in this sense results in variety in the levels' stories. A long level, with various points to rest, but difficult jumps to perform, feels tense, stressful. However, a short level, with near-to-no points to rest, but comparably easy jumps, feels vigorous, yet satisfying to complete. The safety and length of a level creates an overall perceived difficulty of the level, which can be balanced to stay constant throughout the game, even with such a variety of difficulty in platformer movements. Safety brings about variety, without whiplash, overwhelming the player.

Celeste's overall areas play a significant impact too, particularly with pacing and difficulty, but it's clear that, even down to the most miniscule parts of level design, Celeste aims to strive for three main things:
1. Accessibility, through the level's various solutions to one problem.
2. Variation, through examination of the level's safety, length, and perceived difficulty.
3. Intrigue, through the guarantee of an interesting story.