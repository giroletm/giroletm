# *Not* in short — My full programmer's life story
## Preamble
Most of my past works mentionned here will not have links given.

This is to avoid this account to be linked with my other ones, though by giving a little search to your favourite search engine, you can find the tools I mentionned and from there, all the rest of my stuff.

## NSMBW modding — 2017-Today
That actually represents an enormous part of my life. My first attempts at it were around mid-late 2017, but I started to get a decent level around 2020 and I'm still going at the time of writing, August 2022.

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
* A tool to simplify the generation for YAML files used to create new actors in NSMBW

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

This byte-sending program, however, would have needed to be possible to changed to be able to send any byte the control station desires. But while the programs the micro:bit cards used were made in python, these would need to be converted into a format the card would understand before being sent to it.

This format however, was highly undocumented. I had to figure out myself how it worked by guessing and by reading the source code of the IDE that converted python programs to said format.

I ended up writing a 20 pages simplistic manual about my journey through making this control station, including how did this format work and how did I do to edit it in real time.

Our project was then chosen to participate to the 13th edition of the *Olympiades de Sciences de l'Ingénieur de l'académie de Dijon*, so we went to Dijon (yes that's where Dijon mustard comes from) to participate. We didn't get any prize, though another team from my school did so I guess I'm happy for them. After all, the real adventure is the friends we made along the way, or something..?

## Other works

### Programming club — 2016-2017
From 2016 to 2017 I was in a sort of independant programming club where we were taught the basics of C# to make a basic [Unity](https://unity.com/) game.

It started as a basic bowling game, then it expanded to a game with a basic controllable character, an enemy that would try to kill them and collectibles.

### Discord bot — 2018-2021
In April 2018 I made a discord bot in Java for a private roleplay Discord serber themed around a restaurant owned by [Chef Kawasaki](https://kirby.fandom.com/wiki/Chef_Kawasaki).

When talking in the chat, a user would recieve a certain amount of money, in a currency called the *Kawadollard*.

Then, by typing a certain command in the chat, they'd receive the list of aailable dishes along with their price, and could buy one of them using another command.

The bot would then send a picture of the requested dish (as a "here's your dish" message) and take away the amount of money corresponding to the dish's price to the user.

The bot also had admin commands that used a power system (with a power of 0 being a regular user, 50 being a moderator and 150 being an admin) that allowed to mess a little with it, like adding or taking away money from users, or making the bot send a given message in a given channel.

After 7 months, the server closed and re-opened in May 2019 for two months. The bot received a 2.0 update, which included new dishes and games such as Tic-Tac-Toe

Then after closing once again, the server came back for a third season in March 2020 during the lockdown, again for a duration of two months. I added new dishes and updated the bot to the latest versions of the Java Discord bot library.

With the COVID and heat wave, the server's fourth season arrived early in August 2020 (for two months again) with a completely rewritten dish system and better money handling and transfer.

Finally, in July 2021, the server had its fifth and final season to date, for a duration of two months again. The bot reveived its most significant update: a full gestion game was in the works for people to harvest their own ingredients and try creating dishes using them, with common failures but rewarding successes! Unfortunately, it couldn't be finished in time. Some QoL changes were also made, like a daily salary that'd be higher for more active users.

I'd love to resume this project one day and make a sixth season, but for that I'd need to find the motivation to finish the gestion game! Though who knows, maybe during summer 2023...

### Misc tools — 2019-Today

Everytime I need to automate something on my computer, I took the habit of making a tool for it.

Need to batch-convert a file from a format to another? Write a program for it. Need to add or subtract a given number to each number found in a text file? Write a program for it.

You know, this kind of small programs.

## Conclusion

This wraps up my "Who am I?" list, hope you enjoyed reading through it!

I'll try to make yearly updates to this with new experiences I may go through over time.

Thanks for reading!

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Matthieu GIROLET, August 30th 2022
