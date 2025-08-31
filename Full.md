# *Not* in short — My full programmer's life story
## Preamble
Most of my past works mentionned here will not have any links given.

This is to avoid this account to be linked with my other ones, though by giving a little search on your favourite search engine, you can find the tools I mentionned and from there, all the rest of my stuff.

## NSMBW modding — 2017-2022
That actually represents an enormous part of my life. My first attempts at it were around mid-late 2017, but I started to get a decent level around 2020. I stopped doing it regularly in late 2022, but I'm still doing some things from time to time when I feel like it.

For starters, NSMBW, or [New Super Mario Bros. Wii](https://wikipedia.org/wiki/New_Super_Mario_Bros._Wii) is a [Nintendo Wii](https://wikipedia.org/wiki/Wii) game released in 2009.

My main modding activity on that game was programming, of course. But before that, I gave a try to level design, tileset design, and I unfortunately suck at all that.

But in late 2018, I got to compile [NewerSMBW](https://newerteam.com/wii/)'s [source code](https://github.com/Newer-Team/NewerSMBW/tree/clang-no-translations), which is the main place to start on to get to NSMBW Programming.

At first it mainly consisted of C++, but I eventually got to learn PowerPC Assembly which expanded my modding abilities by A LOT. Absolutely anything can be removed, changed or added in the game using C++ and PowerPC Assembly.

Pretty much all of my pre-2023 programming experience came from there, and it also gave me quite some reverse-engineering experience that I hope to be able to use in the future.

## C# Tools — 2019-Today
I've made *plenty* of CLI and GUI tools in C#, most of them being related in a way or another to [NSMBW](https://wikipedia.org/wiki/New_Super_Mario_Bros._Wii).

Notable tools I've made are:

CLI:
* A tool to patch Nintendo Wii roms with other files using a standardized XML file
* A tool to patch Nintendo Wii executables using a standardized XML file (bundled with the former one)

GUI:
* Save File editors for [NSMB](https://wikipedia.org/wiki/New_Super_Mario_Bros.), [NSMBW](https://wikipedia.org/wiki/New_Super_Mario_Bros._Wii) and [NSMBU](https://wikipedia.org/wiki/New_Super_Mario_Bros._U)
* Editors for the Cutscene and Credit Dance file formats used in [NewerSMBW](https://newerteam.com/wii/)
* A tool to simplify the generation of YAML files used to create new actors in NSMBW
* Recently made an [Angry Birds](https://wikipedia.org/wiki/Angry_Birds) modding tool. For now it only allows for spritesheet edition.

## Guide Robot — 2021-2022
During my last year of High school (*terminale* in french, 12th grade in the US) in a technology-oriented course, I was tasked, along with three other classmates, to make a mini robot that'd guide people through the different rooms during the school's open day.

The project would be done in two parts:
* A control station that'd have an interface on which people could choose where they want to go and see a map of the building with the path highlighted, along with the possibility to task the robot to guide them to the room
* The robot itself, which used a [BBC micro:bit](https://microbit.org/) card and would receive its path from the control station using radio waves, then guide itself by using beacons (represented by other micro:bit cards) place throughout the building

One of my classmates was tasked to make an outer shell for the control station, the two others were tasked to make the robot's and beacons' program and I was tasked to make the control station's program.

In the end, I did not only my task, but also the robot and its beacons due to my two classmates having no experience whatsoever with programming and the few programming classes we had being widely incomplete.

Absolute thanks to my last classmate who made the control station's outer shell because him and I are the only ones who actually worked on this project in the end

The robot and its beacon were programmed in Python (using the micro:python module) and the control station's program was programmed in C# (using the Windows Forms lib for the front-end)

I did hit one major obstacle when making the control station however: I needed to transfer the robot its path, but I didn't want to have pre-fabricated programs for each path possibility, as I wanted anyone to be able to add, edit or remove paths from the control station's data without touching to any code.

The way the paths are transfered to the robot is using yet another micro:bit card, connected to the control station, that'd send the path to follow as bytes using a program the control station would put in said card.

This byte-sending program, however, would have needed to be possible to change, to be able to send any byte the control station desires. But while the programs the micro:bit cards used were made in python, these would need to be converted into a format the card would understand before being sent to it.

This format however, was highly undocumented. I had to figure out myself how it worked by guessing and by reading the source code of the IDE that converted python programs to said format.

I ended up writing a 20 pages simplistic manual about my journey through making this control station, including how did this format work and how did I do to edit it in real time.

Our project was then chosen to participate to the 13th edition of the *Olympiades de Sciences de l'Ingénieur de l'académie de Dijon*, so we went to Dijon (yes that's where Dijon mustard comes from) to participate. We didn't get any prize, though another team from my school did so I guess I'm happy for them. After all, the real adventure is the friends we made along the way, or something..?

## Other works

### Programming club — 2016-2017
From 2016 to 2017 I was in a sort of independant programming club where we were taught the basics of C# to make a basic [Unity](https://unity.com/) game.

It started as a basic bowling game, then it expanded to a game with a basic controllable character, an enemy that would try to kill them and collectibles.

### Discord bot — 2018-2021
In April 2018 I made a discord bot in Java for a private roleplay Discord server themed around a restaurant owned by [Chef Kawasaki](https://kirby.fandom.com/wiki/Chef_Kawasaki).

When talking in the chat, a user would recieve a certain amount of money, in a currency called the *Kawadollard*.

Then, by typing a certain command in the chat, they'd receive the list of available dishes along with their price, and could buy one of them using another command.

The bot would then send a picture of the requested dish (as a "here's your dish" message) and take away the amount of money corresponding to the dish's price to the user.

The bot also had admin commands that used a power system (with a power of 0 being a regular user, 50 being a moderator and 150 being an admin) that allowed to mess a little with it, like adding or taking away money from users, or making the bot send a given message in a given channel.

After 7 months, the server closed and re-opened in May 2019 for two months. The bot received a 2.0 update, which included new dishes and games such as Tic-Tac-Toe

Then after closing once again, the server came back for a third season in March 2020 during the lockdown, again for a duration of two months. I added new dishes and updated the bot to the latest versions of the Java Discord bot library.

With the COVID and heat wave, the server's fourth season arrived early in August 2020 (for two months again) with a completely rewritten dish system and better money handling and transfer.

Finally, in July 2021, the server had its fifth and final season to date, for a duration of two months again. The bot reveived its most significant update: a full gestion game was in the works for people to harvest their own ingredients and try creating dishes using them, with common failures but rewarding successes! Unfortunately, it couldn't be finished in time. Some QoL changes were also made, like a daily salary that'd be higher for more active users.

I'd love to resume this project one day and make a sixth season, but for that I'd need to find the motivation to finish the gestion game! Though who knows, maybe during summer 2024...

### Misc tools — 2019-Today

Everytime I need to automate something on my computer, I took the habit of making a tool for it.

Need to batch-convert a file from a format to another? Write a program for it. Need to add or subtract a given number to each number found in a text file? Write a program for it.

You know, this kind of small programs.

## University — 2022-Today

I started attending University in September 2022. My course's name is *"BUT Informatique, Parcours Réalisation d'applications : conception, développement, validation"*.

To put it in actual words, it's a computer science course focused on app design, development and validation. (By "app" I don't mean mobile apps, I mean any kind of apps. I guess the better word here would be "software".)

My course is done in three years, so it's expected to end around July 2025 for me.

On this section, I'll write little journal entries about how I feel there and what I've learnt so far.

### Entry 1: March 9th 2023

This entire uni thing went a lot better than I actually expected (besides a few points ofc).

#### What I have learnt & my feelings

During the first semester, we learnt:
* Programming concepts basics (using C++)
* HTML/CSS basics, some bits of JS
* Computer architecture basics (using [Logisim](http://www.cburch.com/logisim/|Logisim))
* Database basics (Both theoratically and practically using SQL)
* OS basics (more like Linux basics honestly)

I knew most of the C++ stuff we talked about, but the rest was pretty much new to me. I was absolutely mind blown by the computer architecture classes, even if I already have some experience with it as I've written PowerPC assembly during the past two years.

So yeah, good stuff! Though I expected a little more on the web part: we didn't go very in-depth with JS and we barely mentionned PHP. Hope I'll be able to get better at that eventually, because as of right now I'm pretty much unable to make a decent website.

However, the most surprising part about it is the fact that I made friends. That was the part I was the most afraid about, and it went so well! I don't eat alone during lunch anymore, and I have people to speak to, that's nice!

#### My grades

Now of course, I absolutely need to talk about my grades. I'm quite proud of them and I think it might be useful to expose them here.

We split grades into six modules, in which our average is split. There's no "global" average, it's six averages with a given name.
A lot of grades count in multiple modules, so some averages are quite close.

Please note that here in France, our grades are written out of 20 points, not as a percentage:
* Create an app: 19.87/20 (rank 1/26)
* Optimize an app: 19.86/20 (rank 1/26)
* Manage, deploy and maintain a computer or an app: 17.66/20 (rank 1/26)
* Handle data and a database: 16.92/20 (rank 1/26)
* Running a project: 14.40/20 (rank 5/26)
* Work as a team: 14.61/20 (rank 8/26)

So yeah, good stuff, quite proud of the ranks mostly.
The names of each modules aren't very faithful with the things they contain, so don't focus on them.

That's the end of this entry! I think I'll make some of the projects we worked on available to the public someday.

**EDIT:** The first year projects I have made public are available here: https://github.com/giroletm/uB-B1-SAE

### Entry 2: June 29th 2023

Well, that's the end of the first year. Two more to go!

#### Future work

I have found a company to have a [dual education](https://en.wikipedia.org/wiki/Dual_education_system) along university.

I'll get a lot more experience in there. It'll be nice to finally go from theory and personal projects to actual work.
I obviously can't say anything precise abotu what I'll do there, but I can tell you that I'll mainly write C# code.

#### University projects

Now on the uni side, there is something I don't think I have talked about before here that I need to explain.

Each semester, we have a set of projects to do called "SAÉ" ([Situation d'Apprentissage et d'évaluation](https://fr.wikipedia.org/wiki/Situation_d%27apprentissage_et_d%27%C3%A9valuation)).
In the first year, we have a whopping six projects to work on per semester, for a total of twelve, which is one project per module (Cf. Entry 1) per semester (6 modules × 2 semesters = 12 projects).

So I'd like to talk about some of them (mostly the ones I enjoyed) to share some of what I have learnt along the way (and to brag a little bit, let's be honest).

Also, I did ask for permission to the people I worked on these projects with to have their part of the work included here.

##### The first project: Command line games (SAÉ 1.01)

Our first project consisted into making small games in a CLI.

![The project's titlescreen](https://github.com/giroletm/giroletm/blob/main/Resources/READMEFull/Entry2/SAE101-Titlescreen.png?raw=true)

*The project's titlescreen*

Very basic but works well. The available games are:
* Pong
* Snake
* [m,n,k-game](https://en.wikipedia.org/wiki/M,n,k-game)
* [Nim](https://en.wikipedia.org/wiki/Nim)
* Rock, Paper, Scissors
* [Connect 4](https://en.wikipedia.org/wiki/Connect_Four)
* [Blackjack](https://en.wikipedia.org/wiki/Blackjack)
* A Pokémon fight simulator

I made the first four games, whereas my three groupmates made the remaining four.

I also made a highscores system, allowing you to save your name and score whenever you beat the previous highscore.
Your name and score then gets stored into a file to be re-opened whenever you restart the game.

All of this was written in pure C++.

=> [Source code](https://github.com/giroletm/uB-B1-SAE/tree/master/S1_01)

##### An AI project (SAÉ 1.02)

In parallel to other projects that will go unmentionned here, we had a project that consisted into writing an AI to play [Hexapawn](https://en.wikipedia.org/wiki/Hexapawn).

The point was to write multiple AIs that would follow a simple principe, and the end goal was to have the best compromise between code efficiency and game proficiency.

So, me and my two groupmates made three AIs:
* The tree approach: calculate every board possibility as a tree and give scores to each branches, then play the move that has the highest score.
* The score by square approach: simulate a given number of games and give a higher score to squares that often lead to victories. Then, choose the move that leads your pawns to the most strategic squares
* The score by pawn approach: simulate a given number of games and give a higher score to pawns that often win. Then, play those more often than others.

I programmed the first one, and my groupmates did the other two.

If you ever worked with code complexity, you might have already figured out that while the first one wins a lot, it is very long to calculate possibilities and therefore can't work in a reasonable amount of time for a game board as large as 5×5.

The other two AIs however, while they loose more often, work for pretty much any board size if you cap the simulation count.

Ah and, of course, we have written this in C++, and also have made a 13 pages long report to describe our choices, difficulties and solutions.

=> [Source code](https://github.com/giroletm/uB-B1-SAE/tree/master/S1_02)

##### A game (SAÉ 2.01 & 2.05)

Okay, true, there might be a liiiiittle gap between this and the previous projects.
But well, between semesters 1 and 2, we gained a lot of experience!

So the final project of the second semester was to make a board game (of a size of at least 10×10), with elements in each square and the possibility to interact with them using the arrow keys, buttons, a drag-and-drop system, etc.

To put it simply, we obliterated the initial guidelines: 

![Gameplay from the project](https://github.com/giroletm/giroletm/blob/main/Resources/READMEFull/Entry2/SAE201205-Gameplay.png?raw=true)

We made an RPG, with a fully designed map, building interiors, and even a main quest with a little storyline for the game.

All of this, in four weeks, in C++, using [SDL2](https://www.libsdl.org/) for graphics rendering.

I programmed the various internal systems the game works with (actor system, state machine, map system, etc).
One of my groupmates did all of the design and also programmed the inventory system, whereas my other groupmates programmed the characters (Player & NPCs) and the textbox system.

We even had a friend of mine making musics for the game. We also took textures and sound effects from (respectively) [RPG Maker](https://www.rpgmakerweb.com/) and [Untertale](https://undertale.com/).

That was a lot of work for a short amount of time, but we succeeded.

=> [Source code](https://github.com/giroletm/uB-B1-SAE/tree/master/S2_01-S2_05)

##### SAÉ All stars (The unmentionned ones)

Since I'm not going to mention all projects, here is a list of all unmentionned ones:
* [SAÉ 1.03](https://github.com/giroletm/uB-B1-SAE/tree/master/S1_03): Setting up a computer for two clients: a familly and a student
* [SAÉ 1.04](https://github.com/giroletm/uB-B1-SAE/tree/master/S1_04): Creating a database according to a client's constraints
* SAÉ 1.05: Developping a client's showcase website
* SAÉ 1.06: Analyzing the economy side of an IT-specialized company
* [SAÉ 2.02](https://github.com/giroletm/uB-B1-SAE/tree/master/S2_02): Writing an algorithm to find the shortest path between two points on a map that has different constraints on each and every area
* [SAÉ 2.03](https://github.com/giroletm/uB-B1-SAE/tree/master/S2_03): Making a instant [IRC](https://en.wikipedia.org/wiki/Internet_Relay_Chat)-like chat app that works using a client-server system through a local network
* [SAÉ 2.04](https://github.com/giroletm/uB-B1-SAE/tree/master/S2_04): Turning a set of [CSV files](https://en.wikipedia.org/wiki/Comma-separated_values) into a working database and create diagrams to study the data contained within it
* SAÉ 2.06: Organizing the welcome day for next year's batch of students

I will soon enough make a repository with the codes of all project, I'll add a link here once that's done.

**EDIT:** The first year projects I have made public are available here: https://github.com/giroletm/uB-B1-SAE

#### End words

See you next year ;)

### Entry 3: April 9th 2024

My second year is three quarters done, so I'd like to talk about what happened since last time.

#### Apprenticeship

Since mid-August 2023, I'm in [dual education](https://en.wikipedia.org/wiki/Dual_education_system) at an IT company.

I have made immense progress there, and discovered some technologies i hadn't ever used before, such as:
- [Typescript](https://www.typescriptlang.org/)
- [Angular](https://angular.io/)
- [ASP.NET](https://www.asp.net/) ([MVC](https://en.wikipedia.org/wiki/ASP.NET_MVC) & [Razor](https://learn.microsoft.com/aspnet/core/razor-pages/)) 

But I was also able to work on things I had already used before:
- C#
- HTML/CSS/Javascript

I still have a hear and a half to do there, I hope everything goes right.

#### University projects

In the second year, we only get two [SAÉ](https://fr.wikipedia.org/wiki/Situation_d%27apprentissage_et_d%27%C3%A9valuation)s: one per semester.

The first semester's offered multiple subjects. My group's was about creating a website that lets users program AIs.

I will talk about the second semester's once it's finished, in a future entry.

##### Developing an application (SAÉ 3.01)

This project consisted in the creation of a website named "DOTS" for "Drones Out There Searching".

Its concept and name come from the mind of one of our teacher, who acted as our client in this project.

On paper, it's simple: players from the entire world can log into the website to program artificial intelligences (AI) easily and then make them fight each other.

There are two types of AI:
- Target AIs. They win if they can escape from the searching AI in a given amount of time.
- Searcher AIs. They win if they can catch the Target AI.

Both AIs can move on a grid, which can be more or less full of obstacles depending of the game mode.

In a fight between two AIs, each player programs one of them.

Each player has a library they can store and edit their AIs in.
They also can publish them so other players can fight them, and they can use them to fight other players' AIs.

Each player has an Elo value that represents their skills.
Some Elo amounts will make the player level up, giving them access to new features.

We have programmed the visible part of the website ("front-end") with [Angular](https://angular.io/) since I had gotten experience with it thanks to my dual education.

The behind of the website ("back-end") was programmed in [PHP](https://www.php.net/).


To be honest, we have handled our time very poorly during this project, leading us to deliver something of a poor quality compared to the initial expectations we had.

But this isn't a complete loss: even though we couldn't deliver a good quality product, this experience clearly educated us and you can be sure that we won't ever do the same mistakes.

### Entry 4: August 31st 2025

It's been a long time, huh?

I finished my third year of [BUT](https://en.wikipedia.org/wiki/Bachelor_universitaire_de_technologie), my oral presentation for my internship is done, and now I can only wait for the jury to give me my success certificate!

#### Apprenticeship

Everything went well in the company where I worked. In retrospect, I think I as very lucky to find such a great company: I led projects almost entirely by myself, I has awesome colleagues, and I got along well with my apprenticeship manager.

I learned so much there, both in programming and in project management.
Thanks to everyone who helped me there!

#### University projects

##### Developing a complex application (SAÉ 4.01)

I didn't mention it in the previous entry, but the [SAÉ](https://fr.wikipedia.org/wiki/Situation_d%27apprentissage_et_d%27%C3%A9valuation) of the 4th semester was in three parts:

- Using the code of a website developped by the students of the previous year, make an audit of all its problems, suggest solutions to those, and propose new features to add.
  
  Honestly, the hardest part was to get the projet we were given to work, and to understand how it worked.
  
  In the end, my teammates and I have written a 30 pages report.

- We were given 5 commercial PDF files, and 5 JSON files containing a transcription for each of them, made with a tool which, notably, used OCR. We ha to write a Python script that analyzed those transcriptions to output a file that contains the various title levels for each document from a configuration file, so it could theoratically be fed another similarely made file to detect its titles.
  
  The transcriptor was very random, it notably divided some texts for no reason, et wouldn't specify some capital information like font size.

  In the end, we wrote a decent program, and made an interface to create the configuration files.

- As three mini-exercices, we had to solve the first one, and one of the two others:

  - Write an algorithm that can solve a Sudoku from some numbers given at the start.

  - Write an algorithm that, from areas on a hexagonal map with each areas being of one of four possible colors, can compute each area's color so no area touches another one with the same color.

  - Write an algorithm that, from a chess board, can solve the [eight queens puzzle](https://en.wikipedia.org/wiki/Eight_queens_puzzle).

These projets went well, even though there was some frustration due to the fact that:

- We we told there would be a second part only when we finished the first one, and that there would be a third one only when we finished the second one

- Only the second part was graded in the end, so it feels like we worked on the first and third parts "for nothing" ("Yes but you're working for yourself" is not and won't ever be an argument in a university context where time is lacking)

##### Advanced development (SAÉ 5.01)

We could make up any subject we want, so long as we made an application that fills a need and involves a database.

We made a students gestion tool for [Hogwarts](https://en.wikipedia.org/wiki/Hogwarts), which would both act as a student educational resource containing classes, potion recipes, quizes, but also a tool for professors, who could enter grades, homework, and manage students.

In the end, there was way too much to do, and with the lack of time due to the apprenticeship, and honestly, the lack of motivation, some features had to be cancelled, so our project wasn't working well.

With that, the project used technologies we didn't master completely (most notably, NextJS & Symfony), and some members of the team didn't work as fast as we expected.

All of these problems were also present in the oral presentation we had to do on the matter, which was clearly not up to the jury's standards, not up to mine.

However, this is not a full defeat: the errors we made during this project, we now know them and we won't do them again!

##### Evolution of an existing application (SAÉ 6.01)

This last project consisted in upgrading the prevous one to add quality management tools (SonarQube, ESLint, PHPCSFixer, ...), conventions (naming of commits, code organization ....=), and security issues detectors (Drpendabot on GitHub, ...).

We also had to add some features to the application, and write a report explaining it all.

##### Conclusion on projets

Honestly, it's a very good concept!

Sure, the projets of the first years were much "funnier" than the next ones, but either way, it was a good occasion to put our skills in practice, reinforce them, and learn new things.

I will try to make as many of my projects accessible, there already is a repository [for my first year projects](https://github.com/giroletm/uB-B1-SAE), I'll try to make more for the rest!

##### Future

I was accepted into an engineering school in [Île-de-France](https://en.wikipedia.org/wiki/%C3%8Ele-de-France), with an apprenticeship at the [SNCF](https://en.wikipedia.org/wiki/SNCF).

So, the adventure of studies keeps going! I'm going back to school tomorrow!

I will keep updating this document as I can, let's hope things stay positive!

## Conclusion

This wraps up my "Who am I?" list, hope you enjoyed reading through it!

I'll try to make yearly updates to this with new experiences I may go through over time.

Thanks for reading!

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Matthieu GIROLET, March 9th 2023
