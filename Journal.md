# Matrix Clock — Journal Export

- Exported at: 2026-06-26T16:22:05Z
- Project ID: 2001
- Entries: 19

## Entry 1
- ID: 2170
- Author: _PK_
- Created At: 2026-04-14T10:07:53Z

### Content

# April 14th ( Day 1 ) : The Start
So I am planning on making a led matrix display 16x32 but I wanna try 32x64 too I have seen youtube vids and all and always wanted to have one made by myself. So as my desk had some empty space and I heard about fallout this, I knew this was the opportunity to make this. I plan to make my custom PCB I would add audio visualizer and my Spotify song display and I would add a clock

## Started with the 8x8 Dot matrix : FINALLY I GOT SOMETHING TO DISPLAY!! ( IT'S CRAZY I DIDN'T THINK WAS POSSIBLE FOR DAY 1 )
I know my plan is to make a 16x32 or 32x64 display but I chose 8x8 dot matrix to start with cuz its simple and I can get familiar with the MAX7219 and also the coding

So I first understood the basics of led matrix and the concept of Multiplexing

### What actually happens
So say we have a 8x8 64 leds matrix now if I want to control them and I did it by doing it individually for each led I would have to deal with 64 pins which is lengthy process that is why I connect them in 8x8 square grid and then connect such a way that the leds share a positive connection in each row and share a negative connection in each column that way I get 16 pin using these 16 pins I can control all the leds but this still has many pins and few problem.
that is where the MAX7219 IC comes using this I can control the matrix by using only 3 pin So what this does is that the IC takes the data from the microcontroller and uses that for controlling the leds
Now this ic doesn't the All rows simultaneously it actually each row one by one but its so fast that the our eyes don't catch it and brains think of it as a steady image.

I then read about the coding and the MAX72xx [here](https://github.com/MajicDesigns/MD_MAX72XX) this repo taught me a lot though the examples are a bit complex for beginners I suggest search up online for starting the the basic function like mx.setPoint().
Also for easy text I learnt about a library [MD_Parola](https://github.com/majicdesigns/md_parola) it makes it super easy


## What I did today 
1.  I made my Github its very basic and I will refine it soon 
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDU4NywicHVyIjoiYmxvYl9pZCJ9fQ==-3d83a2c0774a6e61638a079155504bc25c06bf18/Opera Snapshot_2026-04-14_142917_github.com.png)

2. I also tried coding and got familiar with the 8x8 dot Matrix
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDU5MCwicHVyIjoiYmxvYl9pZCJ9fQ==--c9f6fd6c4bf6dde3faee3c5ff653ee97185465e5/image.png)

3) I able to control pixels and make basic moving animation of pixels ( But still a lot to learn and change )
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDU5MSwicHVyIjoiYmxvYl9pZCJ9fQ==--e8cc3ffe583c93219a0992c3aa4dc1f4f7a49b9f/image.png)

4) Later I did some research for the actually 16x32 and 32x64 led matrix to take some inspiration and understand what other components I would needing and What will I have to do for the PCB building and CAD making later and searched up which components would be suitable.

5) I later learnt and read about the library MD_Parola and tried some examples of that printing text

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDU5NSwicHVyIjoiYmxvYl9pZCJ9fQ==--c7e1bfac44dba01975bc666806e5f8e96ca9293c/image.png)

IRL pics


![IMG_20260414_152858.jpg](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDU5NiwicHVyIjoiYmxvYl9pZCJ9fQ==--e9fa9b91b127a939bd4cf1c0e563c7be5113c3a1/IMG_20260414_152858.jpg)

![IMG_20260414_152921.jpg](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDU5NywicHVyIjoiYmxvYl9pZCJ9fQ==--bbdbafb5c7545cae1cd63bd1d3526e5480fbab13/IMG_20260414_152921.jpg)

tl;dr I started and researched about my components and the plan for my led matrix I learnt the basics and tried the 8x8 Dot matrix to get familiar with the coding and understand how my project will I used the libraries MD_Parola and Max72xx and made a github repo about the project which I will update and refine later

### Recording Links

- https://lookout.hackclub.com/api/media/1668c2a8-be27-48d7-b602-1f405b2d088d/video.mp4

## Entry 2
- ID: 2335
- Author: _PK_
- Created At: 2026-04-15T14:19:29Z

### Content

# April 15th ( Day 2 ) : Started with the System design

So today I first started with the system design for my project. I thought first I should make a simple block diagram as it would make it easier to understand the data and the Power flow. I was planning on adding text explanation so while making it on Draw.io I added text explaining the power flow and work flow
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDYyMCwicHVyIjoiYmxvYl9pZCJ9fQ==--1f13f7308c41f28a61824d52ee5f9f32ad007017/image.png)

But on the second thought I realised it would be messy and would not look good so I just edit the block diagram and made it simple and then added it to the docs folder on my github repo. I then thought that it a Markdown file would be great to explain the system design and power flow. So I made one on in doc folder and started writing the System architecture ( I searched for a fancy word and got this ).

![Opera Snapshot_2026-04-14_190433_github.com.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDYyMSwicHVyIjoiYmxvYl9pZCJ9fQ==--0f09f8e3f54e92711645137c9d40316495d409f6/Opera Snapshot_2026-04-14_190433_github.com.png)

I plan to describe in detail how the system works and also write the components I would be needing.
This is would help me as I plan to add the BOM too.

I then finalized on this block diagram

![Opera Snapshot_2026-04-14_190657_app.diagrams.net.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDYyMiwicHVyIjoiYmxvYl9pZCJ9fQ==--df5331866013d32ecf5b74c388ef8772473695b1/Opera Snapshot_2026-04-14_190657_app.diagrams.net.png)

The final system architecture md file looks like this :

![Opera Snapshot_2026-04-15_194255_github.com.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDkwNiwicHVyIjoiYmxvYl9pZCJ9fQ==--e2cdfad2d93b84e72792626565e0b49ec6108458/Opera Snapshot_2026-04-15_194255_github.com.png)

I couldn't fit the entire file in the image but go check out my repo. 

tl;dr  I started with design the system and first made a simple block diagram for making the understanding simpler. Then I added it to my github repo in docs folder and added the block diagram and the markdown file called system architecture that describes in detail my system design and work flow and power flow also what components I would be using. 
I also added a BOM file but left it blank as I would edit it later as the total cost and all component are decided especially the price of the PCB I am planning to make

PS : I had to record another 17 min session and edit jounal log for the streak challenge apparently it takes 1 hour logs min. and I made some off screen tiny changes in repo that could have given me few more minutes like changes folder name etc. but I forgot to record them ugh.

### Recording Links

- https://lookout.hackclub.com/api/media/dc3cc2c7-ef87-479d-a89d-181861034887/video.mp4
- https://lookout.hackclub.com/api/media/92f3cc01-9e4d-4a3b-96a0-41aeed0b9bdd/video.mp4

## Entry 3
- ID: 2461
- Author: _PK_
- Created At: 2026-04-16T16:15:28Z

### Content

# April 16th ( Day 3 ) : Lots of typing and Internet Issues!!
Okay so today's day was a lot of typing thinking and searching. So I start the day by writing and planning the firmware. I added a md file in my github repo's doc folder. here I discussed how the firmware would work and its logic I also clarified the User interface there.

![Opera Snapshot_2026-04-16_204250_github.com.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NTEzNywicHVyIjoiYmxvYl9pZCJ9fQ==--5ecac63153d91348fea9fdbe80b987addcb55cce/Opera Snapshot_2026-04-16_204250_github.com.png)

This way it would help me debug in future and would make it easier for people to look at project with things being organised. But then my internet had some issues :( so I had to I break the session **10 FREAKING TIMES** Man my internet service provider said there is a issue it made me my lookout lapses glitchy and I had some errors! Thats why I had to break it in 3 parts. 

Then for the second part of lookout recording I had to redo and change my work cuz the lookout didn't  capture some work due internet issues
Then I moved to the readme and updated it its was not good so I changed it and again the lookout didn't record 10-15 mins work cuz of net issue and I didn't check on it cuz I was busy updating the readme. I was worried at this point cuz the recorded time in the 2 part lookout timelapse was abt 36 min even though it should have been 46-51. I had to hurry for my tuition and I was concerned abt the streak challenge.

![Opera Snapshot_2026-04-16_212601_github.com.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NTE0MCwicHVyIjoiYmxvYl9pZCJ9fQ==--2306f63ea9d26753207e50d9f1f4ed82983177b4/Opera Snapshot_2026-04-16_212601_github.com.png)

But I also made a BOM and its v1 cuz I am sure I will update it later for more components especially when I make the pcb. 

![Opera Snapshot_2026-04-16_212743_github.com.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NTE0MSwicHVyIjoiYmxvYl9pZCJ9fQ==--8ee5372f0643d1aa654a19939af7717535c04379/Opera Snapshot_2026-04-16_212743_github.com.png)

![Opera Snapshot_2026-04-16_212919_www.google.com.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NTE0MiwicHVyIjoiYmxvYl9pZCJ9fQ==--4de1c3df8e0a036950012ab0fb5a6cae49c7dde9/Opera Snapshot_2026-04-16_212919_www.google.com.png)

Later in the third part that I recorded after coming home late I had the net issue again and I had to record atleast 24 min for the streak challenge I then started with writing this Journal Log. I made some edits in readme and BOM and completed this journal log.

TL;DR I made changes in my github repo adding a firmware_plan.md in docs folder and then I update the readme file. I also updated the BOM and added the list of the necessary component though I will change it  in future cuz I will added my PCB price and components too. During all this I had net issues that caused my lookout timelapse to glitch and at times didn't record my work causing about 10-15min time loss as it went unrecorded. I had a really tough time handling this log with the net issues.

PS I request the reviewer if they see this too add atleast another 10-15 min that went unrecorded due net issue plz.
PS I had to record another 2-3 min lookout timelapse cuz due to net issue again the lookout glitch and even though my timelapse was 25 min long it counted it as 23 min which was 1 min short of 1 hour which is necessary for streak challenge


### Recording Links

- https://lookout.hackclub.com/api/media/cd4961f5-97d7-4a6b-a7c0-86f1c1ec53b4/video.mp4
- https://lookout.hackclub.com/api/media/eeab1263-e552-4523-839c-5ddfc5bb9a66/video.mp4
- https://lookout.hackclub.com/api/media/2c3a95cd-953e-461e-83e6-f616b7967285/video.mp4
- https://lookout.hackclub.com/api/media/967afb97-c6f3-495b-a103-30f248bd98fd/video.mp4

## Entry 4
- ID: 2579
- Author: _PK_
- Created At: 2026-04-17T16:59:26Z

### Content

# April 17th : Firmware Started! ( Lots of confusion )

Okay so my experience with firmware is not that good I have written firmware and logic for small Arduino projects but this one is on another level I guess. So today's day was a bit problematic but I managed. So I decided to start with the firmware today I had a clear idea of the logic but then I am not good at coding yet so I searched and well found a [ESP32 HUB75 Matrix Panel DMA library](https://github.com/mrcodetastic/ESP32-HUB75-MatrixPanel-DMA/tree/master) I can use this so I started and tried it.

![Opera Snapshot_2026-04-17_220959_github.com.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NTQwOCwicHVyIjoiYmxvYl9pZCJ9fQ==--c737f88f63dffbfee76c062dc80228d90b98ec89/Opera Snapshot_2026-04-17_220959_github.com.png)

## What I learnt today
Tbh it was confusing at first and well I tried to write code and understand at same time cuz I was recording and well something clicked but the examples were a little complex cuz I don't have much experience with display so after some research I learnt that this library is kinda similar to the MAX7219 MD_Parola like the purpose is kinda same.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NTQwMiwicHVyIjoiYmxvYl9pZCJ9fQ==--da3909cfa775637bf116a5d5084883568bc4b6e3/image.png)

So like those library in the ESP32 HUB75 Matrix Panel DMA library you first define no. of displays and the resolution. Since I didn't have the actual HUB75 matrix panel I could only imagine and understand it.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NTQwMSwicHVyIjoiYmxvYl9pZCJ9fQ==--f070463a42057ee449570c23023401ac61953f8c/image.png)

The basic drawing commands at ->print(), ->drawline(), ->drawrec(). These are the basic functions and well I had some trouble but I slowly understood them. 

Also we can customize the pins for the Led matrix if not defined by us the library will use the default pins for the ESP32.

## Future plan
I plan to understand more and learn more about this library and then move to the next part about RTC module and button input and then in final combine them all tho I believe I will be able to debug them properly when I test them actually in build phase.
I also will learn more about the coding off recording like since staring and idle reading is not allowed I will try to learn first then apply each concept and try it one by one in arduino ide while recording and well I can only imagine cuz I could really test it when I get the component which is after the design phase.


> TlL;DR I started with the code today understood the basics and found out about the ESP32 HUB75 Matrix Panel DMA library. I understood and tried its commands and concept in the arduino IDE and was able to learn about the ->print(), ->drawline(), ->drawrec().  commands which are the basic draw commands soon I will learn and master this library in 3-4 days move to next that is working with the RTC and then when I have tried examples and understood each concept I combine them and write the final firmware I am planning.

PS I nearly had a crashout seeing those complex examples at the Github repo of that library.


Note to reviewer: It might look I was staring at the code or was idle at arduino page or github repo page for 2-3 mins but I changed the code and was thinking about the logic for a minute and lookout happened to take screenshot at that same time.

### Recording Links

- https://lookout.hackclub.com/api/media/54f968b7-3a1b-4258-a2eb-db4a89a7dd5f/video.mp4
- https://lookout.hackclub.com/api/media/032e6b77-b715-42fe-8342-032c221b40b9/video.mp4

## Entry 5
- ID: 3419
- Author: _PK_
- Created At: 2026-04-22T17:41:58Z

### Content

# April 22nd : PCB Schematics and Crash Out!

So I figured I needed to work on coding later and well I had to watch some tutorial to understand other parts of the library I used in previous journal log. So I thought that I will write the final code later and started with PCB schematics today and Man I was so so excited so I started and well first made the setup adding all the necessary symbols of the components I needed.

I plan like the PCB is gonna help me distribute the power to all components and well also connected most of components via trace of the PCB so they are connected. Now I added 2 01x15 socket first ( Actually added 01x19 socket then 01x15 and then 01x17 and then looked online and I finalized the ESP32 Devkit V1 30 pin board so choose the 01x15 this took more time than I thought ). I wanted the pins to be in the right order as the esp32 devkit board as I want it kinda of a socket on which I place and connect the ESP32 board directly no jumper wires cuz that is clean I also had references from the Github repo I looked over in last journal like it had a readymade pcb for this purpose but I thought that would be too easy it didn't many things that I planned to add so I didn't look over it. I then made few connections I followed the connections. ( they were all messy )

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NzAzOCwicHVyIjoiYmxvYl9pZCJ9fQ==--a29eef90f8cc7364560d373712a0e3965ffb3f5d/image.png)

But then I realized something bad I looked up online and had a image of the esp32 board next to me so the order would be right and... The Image was of wrong board so I tried to change the wiring but it was of no use I had actually wired them wrong so I had to then delete the wire I connected. :(

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NzAzOSwicHVyIjoiYmxvYl9pZCJ9fQ==--51c0fa8910a6ad92974bf4a2836e67c5af44ec70/image.png) 

I was so frustrated over this !! but I then had no option and continued and made the connection but its not complete yet. I plan to complete the wire connections for the HUB75 16 pin socket and then the ESP32 and the RTC module in the next session ( also the buttons ).

TL;DR I started with PCB schematics and placed the symbols and made many connection but then realized the pins were wrong connections thats why I had to delete them and start over with connections. _( I WAS SO FRUSTRATED. )_

### Recording Links

- https://lookout.hackclub.com/api/media/6f4b693a-4f55-42ee-b30d-f245225745a9/video.mp4
- https://lookout.hackclub.com/api/media/96d986aa-502d-4b65-a728-c1bbaf01b902/video.mp4

## Entry 6
- ID: 3581
- Author: _PK_
- Created At: 2026-04-23T17:42:59Z

### Content

# April 23rd : PCB Schematics!!

Finally I made the right connections! 

Okay so today's day was progress I finally right PCB Schematics. most of it is done the major Important part that is the  ESP32 GPIO and HUB75 16 pins connector is done. I am pretty happy with today's progress I hope the connections are correct mostly. 

- The start:

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NzM4OCwicHVyIjoiYmxvYl9pZCJ9fQ==--74432b931751dcffd574cbf1668572ce2579fa18/image.png)

- While editing :

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NzM4NywicHVyIjoiYmxvYl9pZCJ9fQ==--eee74d76535ce141a3ea2f1babb7032017f4fd63/image.png)

- Final progress till today :

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NzM2OCwicHVyIjoiYmxvYl9pZCJ9fQ==--099b841dfc335636f8b052c592d96052dc29b804/image.png)

Also I had listed the schematics like data flow and power flow all the connections in my GitHub repo like in its docs folder it has all that info in detail. [Here's the link to my GitHub repo.](https://github.com/pranay-k4/Led-Matrix-Display)

For backup if I mess up one or two wire so the female socket can't be directly to the ESP32 pins so I will I have to use the jumper wires like I am gonna use for the HUB75.
I am really tired Right now this is the only work I did today and well I don't have much photos cuz I didn't took much during the recording but the Lookout timelapse will have it all.
I plan to finish the Schematic tomorrow and start the PCB designing and maybe routing if I have time and don't mess up.

**NO TL;DR SUMMARY TODAY** cuz I am tired and sleepy today its really late at night (about 11pm) I need to log this journal entry fast and text part is not that big and not many images you can see the timelapse for the schematics editing I made.

 _( Also I was frustrated cuz right after I logged in the journal log yesterday I realized I could have changed the connection in code of the library it would be slight lengthy but not as long the time it went messing up schematic yesterday!! BUT anyways I messed up and didn't realize so here we are )._

_Note to reviewer: I know at times like two or three screenshots in the lookout timelapse might look same but I swear I was either adding a wire or was editing the label name the label name menu is actually not recorded also I was checking the connection simultaneously._






### Recording Links

- https://lookout.hackclub.com/api/media/e6b908d1-7a8f-45b1-9ada-059d31921988/video.mp4

## Entry 7
- ID: 3738
- Author: _PK_
- Created At: 2026-04-24T17:32:10Z

### Content

# April 24th : Schematics Finished!! 

FINALLY SCHEMATICS IS DONE!! ( AND ITS ORGANISED ).

Okay so today was a amazing day cuz I had some real progress. So as you know I started Schematics two days ago and messed up day before but was okay yesterday.  But that schematics yesterday was just functionable yesterday and it was a messy of wires. 

I finally finished the Schematics and am sooooo happy as it looks so clean. ( I was so proud of myself that I patted myself ). Cuz I first finished the schematic and wiring and well it looked so messy like wires overlapping each other and very long it was a mess.

So I used labels!! I know I should have used them from start but like I was unsure as the net labels in my KiCad kinda look like floating text and I saw other peoples KiCad they looked like tags but I then realized that its normal after I searched it up online. 

So final grand reveal of this schematic is here: 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NzY4MCwicHVyIjoiYmxvYl9pZCJ9fQ==--1051143660f61e2bfae9aa6d26ba5d11ab6ff1cf/image.png)
 
I plan to add the footprint and start the PCB tomorrow.

No TL;DR as the text part very small today I am sorry I know the journal logs should be long but I just did schematics today and have only 1 image as I didn't took extra while working. You can check the timelapse tho! ( and I am really tired and its late rn )

_PS : There might be a screen in the timelapse where I might look like idle for 3-4 mins or more but its just I was just searching up for the symbol and stuff and adding and deleting it quick cuz it was not the right one the lookout only recorded one screen and not the pop up menu of the symbol so it might look I was but I was not._

### Recording Links

- https://lookout.hackclub.com/api/media/624e8ce2-ceed-4053-8952-4bd262d66b8f/video.mp4

## Entry 8
- ID: 3899
- Author: _PK_
- Created At: 2026-04-25T17:57:15Z

### Content

# April 25th: PCB Finally Started!!


_**Finally I started with the PCB!**_

Okay so today I started the work by first checking the ERC in kicad well it gave 12 FREAKING ERRORS!! I was worried but fortunately they were simple errors and well I quickly fixed 10 of them being me not crossing the unused pins and 2 being about me not PWR FLAG.

This sorted I Moved to Footprint assignment but I paused and realized a problem I added the buttons on the schematic but if I make them soldered on the pcb that will cause problems in me assembling like in cad I will have to adjust and need accurate measurement while making if cuz if I mess up then I might be in trouble so instead I decided to replace them with 2 01x02 Male pin headers cuz that way I solder them and setup easily.

This finally done now I moved to the footprint assignment honestly I didn't have the exact footprint I had to look up internet for the footprint but then finally after few minutes of clicking and typing I have assigned the footprints and now I finally got the fun part PCB Designing and routing!!

So I started with it seeing I am late and won't be able to do much of pcb working I made a rectangle in edge cut and then updated the PCB with the schematic so all my footprints are there and then I finally placed them. This was mostly a rough idea to visualize what will it look like I knew there was much work left and I knew it I can't start routing today so I just placed them and thought of the design. 

I also made few changes with the readme at my Github repo and also added the Schematic to it.

![Opera Snapshot_2026-04-25_231904_github.com.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6ODAyNSwicHVyIjoiYmxvYl9pZCJ9fQ==--b6a7a65049052ca8651948364ad74a7a8ef6f538/Opera Snapshot_2026-04-25_231904_github.com.png)

Tomorrow I plan to make it clean and accurate cuz those ESP32 female pins need to accurate distance or else then I would have to use jumper wires which would be messy. Also start the routing.

So here are the photos of today's work :

-  **PCB Design rough work :**
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6ODAxOCwicHVyIjoiYmxvYl9pZCJ9fQ==--a1ed8d9d7439819b8039f60c74d213fb9af93dbb/image.png)

- **3D View:**
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6ODAxOSwicHVyIjoiYmxvYl9pZCJ9fQ==--2e47e8a000f6866bd3a8b5e04e2a9ee861899055/image.png)

TL;DR I solved few errors that the ERC pointed out then moved to footprint assignment. I also made a change and replaced the button with 01x02 male header pins cuz I plan to connect them separate instead of soldering them on the PCB. I then finally started the PCB designing I started with a basic rectangle and then placed my component on them realizing I can't start routing today I called it a day after making a slight rough design of PCB which def needs work and accurate measurement especially for the ESP32 pins. 



### Recording Links

- https://lookout.hackclub.com/api/media/2153a764-fed2-4b93-b66b-811eade04d6f/video.mp4

## Entry 9
- ID: 4795
- Author: _PK_
- Created At: 2026-05-01T17:53:32Z

### Content

# May 1st : PCB Routing

I was sick so couldn't record and lost my streak but I am back now!!

Done some real progress today first adjusted the component on the PCB and placed them at the right positions especially the ESP32 pin female sockets as they should be at right length that's what I am most worried about if that goes wrong then I will have to use jumper wires.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTAxNTUsInB1ciI6ImJsb2JfaWQifX0=--a885b416fc4d2a51c5b345cb1f4a48679ec54b71/image.png)

Later today I moved on to the routing phase that thing was time taking I wasn't able to finish it entirely but I believe I will tomorrow I guess the routing is really tricky and well I have to do right. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTAxNTYsInB1ciI6ImJsb2JfaWQifX0=--39f43a7369c84f51011ccfb35462806d4f608c03/image.png)

So that was it for today I plan to finish the routing tomorrow and then start and finish the silkscreen layer I wanna add some text for me as guide which pin will be which also make it look pretty cuz its **MY PCB!!**. I will make it look good it gives me extra points.

Oh I think I found some errors and all while I was taking screenshots for the journal I believe I made some errors like the while routing of two pins but I am way to tired to finish this today. So that's it for today.



### Recording Links

- https://lookout.hackclub.com/api/media/ca56046c-5d1b-4ff1-9923-13cf08f35634/video.mp4

## Entry 10
- ID: 5078
- Author: _PK_
- Created At: 2026-05-02T07:41:01Z

### Content

# May 2nd : PCB Finished!! 

It's done!

Okay So I have finished routing the PCB it took a bit especially the part where only a single pin routing was left and I couldn't find a way to connect it but somehow I did it. I ran the DRC thrice just to be sure and the routing was correct.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTAzMzQsInB1ciI6ImJsb2JfaWQifX0=--25a63298faf5b28bceccfc28b2305df837deac35/image.png)

It looks pretty great to me I mean my Second PCB ever ( I built 1st LED chaser at stasis ) and this one looks good to me IDK what the judges will say. So after the routing I moved on to the silkscreen part I labeled every single pin I will be using and made sure its correct according the schematic I am planning and it was great. I ran the DRC again it showed few warnings and I made changes I want 0 errors and 0 warnings
Then I added my initial and credits at the front and bottom layer corners cuz it's mine.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTAzMzUsInB1ciI6ImJsb2JfaWQifX0=--e9560f85850b9ba53fd57627ff6d97eab17d1bd4/image.png)

I also added the PCB file to my GitHub I will add the Gerber files tomorrow.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTAzMzYsInB1ciI6ImJsb2JfaWQifX0=--f6c232bf5d222ee74db7174f764933c652f4b2a4/image.png)

As for my plans for tomorrow I will start maybe CAD or the Zine tomorrow or maybe even the BOM. 
Tasks left to do right now before submitting for review are:
-  CAD
- Zine page
- BOM
- Firmware

And here's the final 3D look of the PCB.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTAzMzcsInB1ciI6ImJsb2JfaWQifX0=--9ed3012846516e9948cff540fd3d539ed0c1088d/image.png)

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTAzMzgsInB1ciI6ImJsb2JfaWQifX0=--05f59233a3f56857d063c0ade9f0572b0ec4f3ea/image.png)

### Recording Links

- https://lookout.hackclub.com/api/media/81892349-01c4-4e71-89c6-29ebdfe8c71d/video.mp4

## Entry 11
- ID: 5265
- Author: _PK_
- Created At: 2026-05-03T11:10:50Z

### Content

# Mat 3rd : Gerber and BOM

Back to the BOM again!

So first things first I made the Gerber files for my PCB and then added that to the JLCPCB shop to see how much it cost its was freaking 9 dollars like the 5 pieces of the PCB itself are just 2 dollar but the shipping cost a freaking 7 dollars I mean WTF that's triple the price of my PCB. At this point I am put so much work in it that I don't feel like removing it from the project I will discuss with the reviewer later maybe about the PCB as maybe just using jumper wires might be a bit cheaper IDK I didn't do the exact math there also I don't wanna think about removing it now. Whatever I will see that later. I mean it might be a little messier but I guess cheaper I will have to do the math for it later like is making the PCB a good idea?

Then I moved on to my GitHub repo and did few things first I changed the BOM. Like entirely first it was a list like in points but now I made it in table format and update adding all the component I needed in a structured way like its neat and looks good I added all the components I would be like almost all I am not sure I might have missed few maybe. So the BOM now has all the components listed ( almost Ig) but like I haven't added the prices and links to websites yet cuz I am still looking for the cheaper options but I will add them soon and also add the Subtotal.
![Opera Snapshot_2026-05-03_162524_github.com.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTA5MTMsInB1ciI6ImJsb2JfaWQifX0=--859cd40330611b93ce93e078fd4fc10e41cc2b35/Opera Snapshot_2026-05-03_162524_github.com.png)

I then paused the Lookout recording cuz I had a quick errand to do that took like 5 mins. Later when I returned I moved to the next part I learnt about license on GitHub previously I had no idea these are free and would help me. So I then made a license for my Project and added it to my repo. But the problem was I didn't unpause when I came back so.... the Lookout didn't record it and 10-15 of work was unrecorded :(.

![Opera Snapshot_2026-05-03_162424_github.com.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTA5MTQsInB1ciI6ImJsb2JfaWQifX0=--75f58e3ee20fa1a7fb99d932071f9ccaf6520634/Opera Snapshot_2026-05-03_162424_github.com.png)

So I well that's it for today I made Gerber files and uploaded them at JLCPCB and added it to my cart. Updated and made the BOM though I still haven't added the final prices and distributors and links but I will do it soon and I also added a License but that was not recorded on the Lookout timelapse cuz I didn't unpause it.

### Recording Links

- https://lookout.hackclub.com/api/media/fa1ccf6f-1430-43c0-8a36-6c28d4ddeddb/video.mp4
- https://lookout.hackclub.com/api/media/02ed8858-317a-4f49-b933-76cb94557df4/video.mp4

## Entry 12
- ID: 5461
- Author: _PK_
- Created At: 2026-05-04T17:48:33Z

### Content

# May 4th: CAD

 _**Happy star wars day!!** ( I am a big fan of star wars I had to do this )_

Okay so last time we finished with the PCB and Gerber and Also Updated the GitHub BOM and added a license. So today we started with CAD well before that I thought of adding mounting holes and fillets to my PCB and opened Kicad but I realized that the holes were a bit big for my small board and I didn't wanna redo the Gerber and JLCPCB thing.

So I opened with OnShape today and made the Fallout folder and started with the CAD. Well I thought of a very basic design for this and well I think it would be best to make a box type enclosure for this LED Matrix So I started with searching the dimensions online and made a rectangle of slight bigger size about 5mm extra each side so I have extra space just in case ( again I might change this later but this is just a start for this CAD ).

Then I made few extrusions and fillets and finally made this its not finished and I am still not sure it looks that good but I will see later 

![Opera Snapshot_2026-05-04_225550_cad.onshape.com.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTE0MDEsInB1ciI6ImJsb2JfaWQifX0=--f7f1ac2513ed82c825bc76754b2c8145d3c0abc5/Opera Snapshot_2026-05-04_225550_cad.onshape.com.png)

![Opera Snapshot_2026-05-04_225550_cad.onshape.com.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTE0MDIsInB1ciI6ImJsb2JfaWQifX0=--d79e455315bcb2a2cb56a639a19c50da6825faee/Opera Snapshot_2026-05-04_225550_cad.onshape.com.png)

I wanna make many changes to this design but I am not sure of it yet. Like for starter I think the design could better and also the other part is the Back cover also I have to make the part for the PCB and the other circuit and then leave make space for the Power outlet. also I am seeing the design and searching for the Grabcad or some inspiration online and well there are quite a few good designs but again they don't have everything like most are just for the HUB75 led matrix panel like they don't cover the other stuff

So I think I will have to work on that and make a better design for this.

I also spend time later today searching for CAD inspiration and the HUB75 prices and all a bit of research for BOM.

**TL;DR** _**Happy Star wars Day !!**_ So I started today with Kicad cuz I thought I should add mounting holes and fillets but I realized they might be slight bigger and I didn't wanna add them so I didn't I later moved to onshape and started making the CAD and its still incomplete but I looked up online for inspiration and did some research for the HUB75 price and CAD designs.

_PS: Its I am there is problem in the Lookout app as it clearly took more screenshots but still recorded few minutes less :(_

### Recording Links

- https://lookout.hackclub.com/api/media/4d42f020-228b-45ee-aa3e-83745cf06e43/video.mp4

## Entry 13
- ID: 6962
- Author: _PK_
- Created At: 2026-05-13T18:01:34Z

### Content

# May 13th : Final BOM!

Yep its final final final BOM. I made the BOM final and all the links are attached I just could not find the link for 1x15 female socket pins 2.54mm but okay they are easily available and well Here are the final updated shots of the BOM. 

![Opera Snapshot_2026-05-13_231156_github.com.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTUyMTgsInB1ciI6ImJsb2JfaWQifX0=--1bee389539456a1a107cbe3cfdb0cc88578ae2fd/Opera Snapshot_2026-05-13_231156_github.com.png)

The only problem today was the HUB75 it is by far the most expensive item and well it really expensive and I really feel a bit unsure about my own project today comparing with what others are making I feel a bit behind.... But I think this is a decent project and well we will have real confusing firmware hope that helps.

Well that's it for today a short entry but I plan to finish the firmware and I think I am ready for that now and well I will also start and maybe finish the zine I plan to submit for review in next 2 two entry minimum.

### Recording Links

- https://lookout.hackclub.com/api/media/d27550a8-df0d-4b49-808c-5ef955bc64f3/video.mp4

## Entry 14
- ID: 7293
- Author: _PK_
- Created At: 2026-05-15T18:03:29Z

### Content

# May 15th : Firmware

okay we are doing the tough and confusing part now.

The firmware has always been my umm bad part I mean I get the logic but my experience with coding is not the best to say the least. So for today's part in firmware I tried setting it up like I added the libraries and well according to how much I learnt by tutorials and all github I think my logic is solid here well I tried to setup the HUB75 Config. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTU5MjgsInB1ciI6ImJsb2JfaWQifX0=--7eb79210ea26aa69469b6ce42d479d83015fc548/image.png)

So after doing that I setup the other things like my RTC and Buttons and variables lots of variables.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTU5MjksInB1ciI6ImJsb2JfaWQifX0=--f91eb7fba050b1844590d154466fc2098a7c8893/image.png)

Then came the void setup and My first mode that Clock mode. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTU5MzAsInB1ciI6ImJsb2JfaWQifX0=--020bbd1549517312f98eabb12fd85dd669e77919/image.png)

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTU5MzIsInB1ciI6ImJsb2JfaWQifX0=--7640ec1fde42c63ebeebee6cfd144c37d9671d8e/image.png)

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTU5MzMsInB1ciI6ImJsb2JfaWQifX0=--e9980ccc18bb1a3f418a9c66d12732e1623b838d/image.png)


This all coding alone took all the time for today's lapse I mean I worried not making any mistake the firmware is not finished but its alr for now I got to check do the other modes and well make the Zine I think this will take 2 more entries. I had a little hiccup recording today like one error when I check the firmware but I guess it might be something cuz the firmware is empty like the void loop is remaining I didn't add it on purpose today I wanna first do all mode and all thing done and then do the void loop. The Loop will be quite smaller compared to the parts in length.

Also I think Matrix Clock would be a better name for my project this old one is quite long and well I think matrix clock is better.

I also added the firmware to my github repo I know its incomplete I will add that note for now I just wanted to see my repo with nearly all parts.

![Opera Snapshot_2026-05-15_233157_github.com.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTU5NDMsInB1ciI6ImJsb2JfaWQifX0=--ef3bf6b2fefb316598954707e15c40967791285a/Opera Snapshot_2026-05-15_233157_github.com.png)


### Recording Links

- https://lookout.hackclub.com/api/media/81af6e15-81cd-4a0a-994a-baa71713b5f6/video.mp4

## Entry 15
- ID: 7398
- Author: _PK_
- Created At: 2026-05-16T11:58:34Z

### Content

May 16th: Firmware done!  and messed up cad
Okay the tricky part is done!

Oh man it was tricky I mean for some reason my Arduino IDE won't compile and tell me if there were any in the codes I think it might some temporary error I will try again later. But just to be sure I manually went through each line and made changes where I missed a semicolon or some error or added a extra space and I uploaded the final firmware on the github repo.

I even added comments and well tried to make it look cool and good and kept it as organized as possible I want it to be readable by others.
 
![Opera Snapshot_2026-05-16_164102_github.com.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTYxNjYsInB1ciI6ImJsb2JfaWQifX0=--38769ca87d0e62daef096a7aa231cebaf983756e/Opera Snapshot_2026-05-16_164102_github.com.png)


Man I love how my repo looks now. I am so proud of myself. Okay so only CAD and Zine are left. Now

> ~ While recording and journaling this log this happened 

Noo!!! I messed up cad 

So here is what happened I wanted to record more so I started onshape and well continued with my cad and well I just made it final everything was going good but then I decied to check my dimension and well checked the hub75 I was going order which I added in my BOM before and well I messed up the pitch of the Matrix display I considered the pitch 3 and made the entire display cad but I added 2.5mm pitch Hub75 and MAN I was worried I tried to fix it but it messed up even further but fortunately I have undo and well I got back to the final CAD well it is for Pitch 3mm

Well I fixed it using undo and here it is now don't judge me plz I have been so much and I the cad is not that good.

![Opera Snapshot_2026-05-16_172457_cad.onshape.com.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTYxNzYsInB1ciI6ImJsb2JfaWQifX0=--b3822dbbf12c95e84b4fb7fb5510985ff4b75c50/Opera Snapshot_2026-05-16_172457_cad.onshape.com.png)


Well that is enough for today I will talk tomorrow and I will see how to fix that pitch and size issue tomorrow you can check the lapse for the errors I made.

### Recording Links

- https://lookout.hackclub.com/api/media/55f176e1-db88-4079-b44f-7029654e3548/video.mp4

## Entry 16
- ID: 7599
- Author: _PK_
- Created At: 2026-05-17T12:31:08Z

### Content

# May 17th: CAD Completed

Man it was a nightmare redoing the enitre cad. Well since I messed up the cad before cuz I used the wrong dimension considering the pitch to be 3 instead of 2.5mm which I actually selected My entire cad enclosure was way to big for the HUB75 P2.5 Led matrix.

And I couldn't find any other way I tried down sizing it manually but cuz the amount of extrusion and sketches I made it showed many errors So I did what I had......

I redid the ENTIRE CAD. That tiring I noted and worked on the exact dimensions this time cross checking with the product I am planning to buy.

Now I know you may why this all work just change and buy the led matrix of p3 instead but I CAN'T. Its expensive like 700-750 rupees that's 7.5-8 $ I can't afford such change and then I moved on and redid and added some touches and well mounting holes too for the LED matrix I am worried about the position actually I will cross check once wait.

>Few minutes later

Okay so I checked and well made some changes like made some extra space for the mounting holes and all I can't verbally explain it best but like two holes very close by like edge to edge and then I I removed some other extra part to get something like this

![Opera Snapshot_2026-05-17_172352_cad.onshape.com.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTY1NjQsInB1ciI6ImJsb2JfaWQifX0=--492190d93d0332d710004163d7351fc9f40af8f5/Opera Snapshot_2026-05-17_172352_cad.onshape.com.png)

Here are the photos of the cad also I uploaded it to the github

![Opera Snapshot_2026-05-17_175124_cad.onshape.com.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTY1NzYsInB1ciI6ImJsb2JfaWQifX0=--8a808503ad88e233380fe9959b5643d7af034283/Opera Snapshot_2026-05-17_175124_cad.onshape.com.png)

![Opera Snapshot_2026-05-17_175236_cad.onshape.com.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTY1NzgsInB1ciI6ImJsb2JfaWQifX0=--665372e448b763661cb1f99fe7dde7a41b7c8077/Opera Snapshot_2026-05-17_175236_cad.onshape.com.png)

Well that is all for today finally everything is done !! Yipeee Wait 

I HAVE TO MAKE THE ZINE AND UPDATE README


_PS: The lapse may have one screenshot of macondo but I wasn't doing macondo the tab was just open and I misclicked on it. _


### Recording Links

- https://lookout.hackclub.com/api/media/109a2bf1-0a88-4f46-b84c-62e869563377/video.mp4

## Entry 17
- ID: 10965
- Author: _PK_
- Created At: 2026-06-01T18:44:59Z

### Content

# 1st June: Zine ( and I AM SICK )

Ahhhh !! I am really really really Frustrated about this one, apparently design is not my field of excellence.

So I am gonna make this entry a short one cuz I am ill and its midnight. So I started the zine design today on canva and well.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjUwMzIsInB1ciI6ImJsb2JfaWQifX0=--3e9bedf74abb0b5cd6c4931e65671dca7b0ce76c/image.png)


I really can't understand how to do it its mostly messy and I don't have any ideas I will talk about this later. I am really tired rn.

_PS : I know this is a bad entry but I am really ill._

### Recording Links

- https://lookout.hackclub.com/api/media/50eb03fd-9ea0-4d4a-89da-386b78e23ba3/video.mp4

## Entry 18
- ID: 12554
- Author: _PK_
- Created At: 2026-06-08T18:09:51Z

### Content

# June 8th : Finished!

Its done the designing phase and all is finally done!

Finally done!

_I am sooo happy rn! I can't express AHSKJSHAKL_

Okay so what I did today quickly was complete the zine and man it looks pretty according to me. Please don't judge I am proud I made that like its good cuz I have zero experience in design and Zine making.
I also made some changes in the CAD it was a huge error I forgot to add the holes for the button  _Still can't believe I forgot that but anyways it fine now!_

And here is the Zine finally have a look 
![Matrix Clock v1.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6Mjk1MzIsInB1ciI6ImJsb2JfaWQifX0=--d8ff2fb324a43937f7c104a3769d9f8a830ea964/Matrix Clock v1.png)


I think its alr I uploaded that to github repo and Then made some changes about the CAD file.


I can't believe its finally done now and I can submit it for build review so happy!


### Recording Links

- https://lookout.hackclub.com/api/media/073e1e48-05b5-4faf-800d-f1032f776490/video.mp4

## Entry 19
- ID: 12562
- Author: _PK_
- Created At: 2026-06-08T18:21:49Z

### Content

# June 8th: 

Okay this is just a another short additional entry I really wanted that my github repo readme looked good before I submit for the review so I made a few changes like the heading size and position and added a quick overview and made some tiny changes.

I forgot to add that and record it in last session so I am adding it quickly here.
![Opera Snapshot_2026-06-08_235011_github.com.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6Mjk1NTYsInB1ciI6ImJsb2JfaWQifX0=--dac613217ade9494a90b7cd2caa98af6bf0b3c87/Opera Snapshot_2026-06-08_235011_github.com.png)


You can check out all the changes I made on [repo](https://github.com/pranay-k4/Matrix-Clock-v1/blob/main/README.md).

### Recording Links

- https://lookout.hackclub.com/api/media/eaa7c4bb-1055-4385-8916-b24b69e6b32b/video.mp4
