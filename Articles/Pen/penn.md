# Index
- [Introduction](#introduction)
	- [The Idea](#the-idea)
	- [Why are there no such pens?](# Why are there no such pens)
- [Design Process](#design-process)
# Introduction
## The idea
I recently came across a mechanical pencil (%%attach picture and/or affiliate link%%) which had the button to extend the mine closer to the tip, in a place which was a lot more convenient to reach during writing.
I am not personally a big Fan of mechanical pencils, but this design element resonated with me and I wanted a similar thing for a ball point pen. Sadly I have not been able to find any ballpoint pen with a similar design, thus I have decided to make my own.
![[edu.jpeg]]
## Why are there no such pens?
The mechanical pencil has the unique feature of the user needing to "refill" the tip as it wears down, thus during extended sessions constant regriping is needed to refill the tip.
This is not a problem when using ball point pens during long sessions, since once you have engaged the tip the user does not need to interact with the main mechanism until they are done.
So why should the manufacturer bother designing a whole new mechanism that will not significantly contribute to the user experience?
This is why I think the main reason why there are no ball point pens with an ergonomic deployment mechanism. Although it is a reasonable explanation to not mass produce such a pen it will not stop me in my pursuit of having such a pen, because the idea brings me joy.
# Design Process
## Goals and Objectives
Before doing any research or opening my CAD software I had to decide what were the goals of my product.
After some thought and observation about my preferences and inspirations I decided upon the following 4 objectives sorted from most to least important to the project.
### 1. Ergonomic and Retractable
As stated in the introduction, this project was inspired by the desire to have an ergonomic deployment method for a retractable ball point pen.
### 2. It should not roll away
I do not enjoy when pens roll away from your control, especially when in a lecture hall where your writing surface is slightly inclined towards you. This can be achieved by making the body not fully cylindrical or by adding a clip.
### 3. Clip or no clip?
For my EDC pens I require them to have a clip by the way I store and carry them, so ideally I would add one. But this would add another component to be designed and more complexity.
### 4. Screwdriver bit
I saw on maker world a pen (%%link!%%) with exchangeable tips to allow for using a standard screwdriver bit in addition to the writing tip (This was actually the first inspiration for this project, because it made me realize that I could 3D-print any pen I could imagine). Having a screwdriver in a pen sounds just like the type of unnecessary but oddly specific feature I love.
## Research
When doing some preliminary research into existing ball point deployment technologies I came across 3 main Mechanisms.
### 1. Clicky button
The Clicky button is the most common mechanism I have experienced, it consists of a button at the very end of the pen that spins a notched plastic piece into place in such a way that it cannot fully retract. When pressing the button again the plastic pieces spins further until it can fully retract when slotting into another groove. Although this is a very elegant mechanism it would not be easy to move it further to the front.
### 2. Turning cap
The turning cap is a relatively common mechanism in which you spin both halves of a pen to extend the tip by engaging a screw joint. This mechanism already is implemented in the front since one of the halves that you spin is the front one. But this design requires two hands to be operated and thus I cannot consider it ergonomic.
### 3. Bolt Action
The Bolt Action pen is a mechanism which I have not encountered in person before, but the interaction looked very attractive and satisfying to me. It consists of pushing down a pin in an "L" shaped channel and turning at the shorter side to lock it in place.
I realized that I could translated this mechanisms to the front of the pen due to the geometry of the ink cartridges that I was planning to use. These had two "wings" close to the tip to engage the spring without needing to use a step making the cartridge wider from that point on. (%%add a picture of wings vs sarasa cartridges%%) This means that I could make a hollow plunger that could press on those "wings" to engage the tip. Making an ergonomic deployment possible.
This mechanism does have the potential issue of retracting accidentally during use and that is why sometimes the channel is Shaped like a "J", which makes retraction more inconvenience since the user needs to push the ink further in to be able to turn it and disengage it. This might be the main reason why I haven't seen many of these pens in the wild, but I am only speculating.
I ended up going with this option an I realized that my design accidentally fixes this problem, since having the pin close to your finger provides for a nice resting place for your finger when writing which if you have the right version (Left vs. Right handed) will prevent the mechanism from disengaging accidentally.
### Other options?
I briefly considered implementing some more exotic (%%lfaw%%) joints and mechanisms like the Scott-Russel linkage, but quickly discarded it in favor for a quicker implementation that already works. Additionally I was already excited about the "wing" realization I had when considering the Bolt action mechanism.
# Version 1 (Sep. 2026)
Version 1 of this pen was a success, there were many things to fix but enough positive ones for me to continue pursuing this idea. Some positive elements were unexpected and embraced in future iterations.
## The Tip
Initially my plan was to attach the tip to the main body of the pen with a screwing tip like in many commercially available pens. Nonetheless I was having issues with the tolerances of 3D printed threads. 
Problem 1: The print quality of the threads was very inconsistent from print to print. There where some prints that had some very clean looking threads and others which were clogged by stringing. 
Problem 2: I had a great difficulty threading the screw. On the one hand my tolerances where way to tight. On the other had, not sure why but the entry way of the female part of the mechanism did not have en entry notch for the thread to bite into.
For the purpose of getting a first prototype as quickly as possible, in order to decide it the my idea was worth pursuing, I made the compromise of ditching the screw lock temporally and instead just use a pressure fit. This did achieve the goal of providing with a first working prototype, but it also introduced some (expected) issues. 
Since the tip was only being held in place by friction and when engaged the spring would try and push the tip out. The tip did from time to time slide out. This was not as big of an issue as I expected at first. The tip only slid out on rare occasions. But it still was an issue I was not willing to have in my final product.
## The Body
### The plunger
I chose to go for the "L" shaped channel, since it was easier to implement on a first prototype and if it didn't work I could always transition to the other geometry later. This turned out to not be necessary since due to the placement of the pin, when using the pen the pin is in a nice resting position for the finger, which it prevents it from unintentionally disengaging, as long as you pick the right chirality.

Speaking of which this pen accidentally has a left and a right handed version, I realized this when I was letting my girlfriend try my pen out and she was struggling to operate it since she was constantly disengaging the type. 
It turns out that I accidentally printed a left handed version and never noticed it when testing it because I am left handed, but after some closer inspection at how we both where using the pen I came to the realization that the pin is a nice resting spot for your fingers and depending on with which hand you would use it that would lead to a more secure locking mechanism or a more insecure one. That is why I will provide the files to both versions.

Another point of decision with the plunger would be the pin, for the purpose of getting a functioning prototype I just used an M2 screw as the pin. At first I thought this would just be a temporary solution and that I would 3D-print something else in subsequent versions, but I don't think I will do that. 
Arguably the pin is the piece of this whole mechanism which will be under the most force and thus metal will always provide more strength than any 3D-printed alternative. Additionally M2 screws are both cheap and readily available, making the assembly process not that much more inconvenient. 
Thus I have decided to keep it for further versions and I would heavily consider it for the final version.

A further problem I found regarding the plunger was a more aesthetic one rather than a mechanical one. The presence of the channel provides a hole into the interior of the pen which exposes the ink cartridge. Originally for the purpose of a cleaner final product I tried to cover it up by making the plunger longer on both sides to permanently cover the whole. This would not have fixed the issued since the channel is at the same height as the wings and the tolerances are too tight to cover the wings and the mechanism to still run smoothly. Thus the way to cover this hole would be to move the channel further up the body of the pen. But I a very happy with the current placement on the channel and I would personally prioritize the ergonomics over the aesthetics, thus I have decided to keep it like it is.
This is also accidentally a feature, since it lets you peek at the ink level and if it is bellow the channel you can add some cartridge replacements to the shopping list. It is not a bug it is a feature.
### The Geometry
In order to make the grip more comfortable I added two groves that traveled along the length of the Pen. These where not a success. I did not make then long enough for the user to interact with them whilst writing. This has made the pen a tad slippery which would be a problem during long sessions.
I have tried holding the pen upside down to engage with the groves and they do make the holding experience more comfortable, although the current placement is weirdly asymmetric. 
Thus I will implement further geometries in the next iterations. CNC Kitchen has made a project to add interesting textures to 3D-prints (%%add link!%%)
### The material
I have printed the first version out of some white PLA, because it was the material I have lying around. But after using it for a few days I noticed some ink stains on the body from not fully dried ink. For my personal version I do not care about this but for the final product I should consider other colors to hide this issue.
The color white did give it an elegant look so maybe I should go for black. But I could also go for the fun route and pick more colorful options.
### Structural integrity
3D-Prints are famously weak to forces applied parallel to the layers. In the current print orientation by that rule of thumb the pen would be weak to bending forces along the long axis. I will need to do further testing to see if it is sufficient. Else I would consider printing the pen on its side to increase its strength. Although it might mess with the overall geometry of the pen, since due to printing limitations you can not print a perfect cylinder on its side (There would be a flat section).
## The But
### The screwdriver
I made a hexagonal slot at the end of the pen, that would fit any standard screw driver bit. In order to secure the bit in place I also added a slot for a magnet at the bottom. This turned out to be a failure. 
Problem 1: The magnets I was planing to use where not strong enough to hold the bit in place during some very scientific shake testing (%%add GIF for comedic effect?%%).
Problem 2: I realized that having an exposed screw bit is quite dangerous and has high piercing potential for any storage container. Thus ideally I would add a cap to conceal the bit. I am not a big fan of pen caps since they add an additional element to keep track of and they are historically one of the most easy things to lose. This is one of the reasons why retractable ball point pens are my preferred tool for writing, since they are self contained and only one piece.
Problem 3: I am converned about the structural integrity of the body already and I am not sure how the pen would handle the twisting forces. Problem 4: Would a good screwdriver handle also be a good pencil handle, or would their geometries be incompatible? This is not necessarily a problem but it is something to take into consideration when designing the geometry of the body.

I think for near future I will abandon this idea, but I might revisit it once I am happy with all other aspects. This feature is defenetely at the bottom of the priority list at the moment.
### The clip
As mentioned above I was inspired by Craighills video about wire clips (%%link!%%) when designing my clip. As a fist proof of concept I used a paper clip, this was ofcorse not the best material to try it, since paperclips are famously deformable. But I liked the result enough to pursue this idea further with better materials.
The paper clips I as using had a rubber coating over the wire which did add a fun splash of color. Not sure how easy it would be to implement when using better wire, but it is something to keep in mind, also for choosing what other PLA colors I can use.
Initial tests with the paper clip showed that it was quite finiky to get the bend in the right place. I am considering to design and print a jig for the production proces, but I will only do that once I have acces to the higher quality wire.
The current clip detaches very easyly. This could be dur to the current attachment point being too narrow or the paper clip being to deformable.
The current attachment method is a rectangular lug with two holes. This is not necessarily bad. But if I consider removing the screwdriver bit, then I could use the whole diameter of the pen for our attachment holes, which might make the clip be more stably attached. I will need to do some testing once I find some good wire.
## What can we improve on?
We have taken a very close look at all elements of Version one, the key take aways from version 1 that I should try to implement into version 2 are:
- Design a more reliable tip attachment
- Mirror the design for a right handed version
- Consider some Pin alternatives for the plunger
- Test some geometries and textures to increase the grip of the body
- Try some other colors
- Compare strength and looks of different orientations
- Try other wire materials and placements
# Version 2 (Oct. 2026)
Version 2 was amazing, most of the issues of Version 1 were fixed and the current flaws are small enough that I am willing to call the project complete. But let us go over what these changes are and what the new problems are.
## The tip
I have made the tip screw in successfully. The main 2 changes I did from my approach of version 1 where to make the screw shorter and making the hole bigger.
When comparing my screw to other pens I had lying around my home I noticed that my screw was way too long at 10mm. Traditional pens have a thread length of at most 5mm, a shorter screw makes replacing the ink a less tedious process.
But I still had the issue of the screw not threading properly. First I increased the tolerances making the distance between threads larger since 3D printing resolution is not that fine, but this did still not solve it. What ended up solving my issue was scaling the body of the pen by 10% only in the x and y axis (Initial tests showed that 5% also works, but 10% feels smoother and just as precise).
Scaling the body up lead to an awkward step between the tip and the body. This I solved by making the tip 10% wider without changing the thread.
## The body
In order to improve the holding experience I have replaced the cylindrical shaft for a hexagonal one (just like in pencils). This significantly improved the holding experience and stops the pen from rolling away even more.
On the topic of improving grip, I also tried out CNC Kitchens tool for adding textures to 3D prints and I have gotten mixed results. The grip did certainly improve but I got mixed responses for the looks. Some users preferred it others called it ugly. Thus I will provide both versions and maybe experiment with a more sutler texture too.
I performed a stress test (I tried to snap the pen in half) on the first version and it failed. In order to increase structural integrity of the pen I tried printing the shaft on its side. This lead to higher strength but also since the pen is now hexagonal all the faces had different an very ruff textures, which was a bit of an eye sore. I have been carrying this pen on my back pocket and I have sat on it numerous times and it has not snapped with the vertical printing orientation. Thus I have decided that for asthetic reasons I will choose the preatier but less strong printing orientation, since the pen is stron enought for regular everyday use.
## The But
As discussed in the first version I have decided to remove the screwdriver bit for the better.
As for the clip I bought thicker and stronger wire and it has given better results. The wire might be a bit thin since it can still deform when opening the clip further than 90 degrees.
Making the wire straight was difficult at first, but I have found this jewelers trick to make wire straight. It consists of holding the wire with a towel and puling the wire between your fingers at a 90 degree angle. If you repeat this process enough times and change the direction of the bend each time the wire will become straight.
# Conclusion
I am very happy with the resulting product and I have been using it on a daily basis for the past few weeks. It brings me joy to use it since it is something I made my self and have put a lot of thought into it, and there is none like it.
The issues from V2 are small enough that they do not bother me, but in case of mass production could be fixed relatively easily by choosing other materials and production methods.
I will be uploading the files to printables and maker world in case you want to make your own ergonomic bolt action pen. As additional materials you will need an ink cartridge with the wings, a pen spring and an M2 bolt for the pin.


---
# Admin
- I when explaining how the different mechanistic work I should provide with pictures or gifs as visual aid to the reader. Because it is very obvious to me, but it might not be the case for an average reader.
- The CNC Kitchen tool for adding textures to 3D prints is called bump mesh
- I can do the gifs in inkscape?
	- Might be too much work --> Low ROI
- The body of a pen is called the barrel
- The but does also have a fancy name, but I do not remember it.
- Add a linked index at the beggining