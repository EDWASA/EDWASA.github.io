<style>
    .content-wrapper {
        display: flex;
        flex-direction: column; /* Stack columns on mobile */
        gap: 2rem;
    }

    .main-content {
        flex: 3;
    }

    .sidebar-block {
        flex: 1;
    }

    @media screen and (min-width: 768px) {
        .content-wrapper {
            flex-direction: row; /* Place columns side-by-side on PC */
        }
    }
</style>

Article written by Eduard Wagener

15th of October 2026

<div class="content-wrapper">
  <div class="main-content">
    # Index
    - [Introduction](#introduction)
    - [Design Process](#design-process)
    - [Version 1](#version-1-september-2026)
    - [Version 2](#version-2-october-2026)
    - [Conclusion](#conclusion)
  </div>
  <div class="sidebar-block">
    <img src="https://edwasa.github.io/Articles/001_Ergonomic_Pen/Media/cover.jpeg" style="width: 100%">
  </div>
</div>

# Introduction
## The idea
I recently came across a mechanical pencil which had the button to extend the mine closer to the tip instead of the end, a place which was a lot more convenient to reach during writing without the need of regripping the pen.

I am not personally a big Fan of mechanical pencils, but this design element resonated with me and I want a similar mechanism for a ball point pen. 
Since I have not been able to find any ballpoint pen with a similar design, which is why I have decided to make my own.
## Why are there no such pens?
The mechanical pencil has the unique flaw of the user needing to "refill" the tip as it wears down, thus during extended writing sessions constant regripping is needed to refill the tip.
This is not a problem when using ball point pens, since once you have engaged the tip the user does not need to interact with the main mechanism until they are done.

So why should the manufacturer bother designing a whole new mechanism that will not significantly contribute to the user experience?
This is why I think there are no such ball point pens. Although it is a reasonable explanation it will not stop me from designing my own ergonomic and retractable ball point pen.
# Design Process
## Goals and Objectives
Before doing any research or opening my CAD software I had to decide what were the goals of my product. These would guide my design and research process.
After some thought and observation about my preferences and inspirations, I decided upon the following 4 objectives sorted from most to least important.

### 1. Ergonomic and Retractable
As stated in the introduction, this project was inspired by the desire to have an ergonomic deployment method for a retractable ball point pen.
### 2. It should not roll away
I do not enjoy when pens roll away from your control. This is particularly of my annoyance when sitting in lecture, since the writing surfaces tend to be inclined towards you.
This can be achieved by not making the barrel fully cylindrical or by adding a clip.
### 3. Clip or no clip?
For my EDC pens I require them to have a clip by the way I store and carry them, so ideally I would add one. 
This could add more complexity and is thus not a high priority.
### 4. Screwdriver bit
The original inspiration that lead me to this projects was [this](https://makerworld.com/models/1440290?appSharePlatform=copy) pen in maker world, which has an interchangeable tip compatible with standard screw driver bits. 
Having a screwdriver in a pen sounds just like the type of unnecessary but oddly specific feature I love.
## Research
First I did some research about existing mechanisms to see if I could adapt any of them to fit my design Goals. During this research I came across 3 main mechanisms.
### 1. Clicky button
The Clicky button is the most common mechanism I have encountered, it consists of a button at the very end of the pen that when pressed spins a notched plastic piece into a shallow grove and can thus not fully retract. When pressing the button again the plastic pieces spins further into a deeper grove allowing it to fully retract.

Although this is a very elegant mechanism it is not clear to me whether it can be moved to somewhere else in the pen. 
For further details on this mechanism check this youtube video: https://youtu.be/Zv5Qa2kGL04?si=GeoqBJl5t0IR3pbY
### 2. Turning cap
The turning cap is another relatively common mechanism in which you spin both halves of a pen in opposite directions to extend the tip by engaging a screw joint.
This mechanism already is implemented in the "front" since one of the halves that you spin is the front one. But this design requires two hands to be operated and thus I cannot consider it ergonomic.
### 3. Bolt Action
The Bolt Action pen has a mechanism which I have only seen online. The tip is extended by pushing down a pin in an "L" shaped channel and turning to the side to lock it in place.

I realized that I could translated this mechanisms to the front of the pen due to the geometry of the ink cartridges that I was planning to use. These had two "wings" close to the tip for the spring to press on. I realized that I could use a hollow plunger to press on the "wings" from the top to extend the tip. This would make an ergonomic placement possible.

<img src="https://edwasa.github.io/Articles/001_Ergonomic_Pen/Media/wings+spring.jpeg" style="width: 350px">

Bolt action mechanisms do have the potential issue of retracting accidentally during use. That is why sometimes the channel is Shaped like a "J", which makes retraction more inconvenience since the user needs to push the ink further in to be able to turn it and disengage it. This ended up having a a nice solution in my design.
### Other options?
I briefly considered implementing some more exotic joints and mechanisms like the [Scott-Russel linkage](https://en.wikipedia.org/wiki/Scott_Russell_linkage), but quickly discarded it in favor for a quicker implementation that already works. Additionally I was already excited about the "wing" realization I had when considering the Bolt action mechanism and wanted to try it out.
# Version 1 (September 2026)
Version 1 of this pen was a success, there are many things to fix but enough positive ones for me to continue pursuing this idea in a second version. Some positive elements were unexpected and will be embraced in future iterations.
## The Tip
Initially my plan was to attach the tip to the barrel of the pen with a screwing tip. Nonetheless I was having issues with the tolerances of 3D printed threads. 
- **Problem 1**: The print quality of the threads was very inconsistent from print to print. There where some prints that had some very clean looking threads and others which were clogged by stringing. 
- **Problem 2**: I had a great difficulty threading the screw because my tolerances where way to tight.
For the purpose of getting a first prototype as a proof of concept, I made the compromise of using a pressure fit for this version.

This introduced some expected issues. Since the tip was only being held in place by friction and when engaged the spring would try and push the tip out. The tip did from time to time slide out. This was not as big of an issue as I expected at first, since the tip only slid out on rare occasions. But it still was an issue I was not willing to have in my final product.
## The Barrel
### The plunger
The plunger consists of a hollow cylinder with a protruding pin to move through the channel.

I chose in this version to use an M2 screw as the pin, since it was the only thing I had lying around that would fit into the narrow channel. This was initially a temporary solution but I have decided to keep it due to 2 main reasons:

1. The pin is one of the pieces that is going to be under the most stress and a metal screw will always be stronger than any 3D printed part of the same dimensions.

2. M2 screws are cheap and easily available for making assembly not that much more inconvenient once I upload it to printables and maker world.

I chose to go for the "L" shaped channel, since it was easier to implement on a first prototype and if it didn't work I could always transition to the other geometry later. 
This turned out to not be necessary due to a lucky coincidence. The placement of the pin is a very nice resting spot for your thumb, which will prevent it from unintentionally disengaging, as long as you pick the right chirality. It turns out that I unintentionally made a right and left handed version of the pen. Which I realized when my partner (right handed) was struggling to use the first version when I (left handed) had no issue.
That is why I will provide the files to both versions.
Once I printed the first version I encountered something I was not expecting. Due to the placement of the channel I could see the ink cartridge through it.

I considered changing the plunger design to cover this hole, but this would only be possible by moving the channel further up defeating the purpose of its placement. Another option to cover the channel would have involved making a thin pad on one of the sides to go over the wings, but the tolerances are already tight enough that I would not want to make the pen wider just to hide the ink, since it is useful to be able to see how much ink is left in the pen (many pens are transparent for this reason). That is why I have decided this is not a bug but a feature of my design.
### The Geometry
The Barrel of the pen was a smooth cylinder, that made the pen a tad slippery which would be a problem during long sessions.
In order to prevent this I added two groves that traveled along the length of the Pen. These where not great, since I did not make then long enough for the user to interact with them whilst writing defeating the purpose of adding them in the first place.
In the next version I will try new geometries that are more comfortable to grip.

Alternatively CNC Kitchen has made a program called [Bump mesh](https://bumpmesh.com/) that allows you to add textures to your 3D prints. I will experiment with these textures to add grip.
### The Color
I have printed the first version out of some white PLA, because it was the material I had immediately available. But after using it for a few days I noticed some ink stains on the pen from not fully dried ink. For my personal version I do not care about this but for the final product I should consider other colors to hide/prevent this issue.
The color white did give it an elegant look so maybe I should go for black. But I could also go for the fun route and pick more colorful options.
### Structural integrity
3D-Prints are famously weak to forces applied parallel to the print layers. In the current print orientation by that rule the pen would be weak to bending forces along the longer axis. 
I will need to do further testing to see if it is sufficiently strong. Else I would consider printing the pen on its side to increase its strength.
## The Butt
### The screwdriver
I made a hexagonal slot at the end of the pen, that would fit a standard screw driver bit. In order to secure the bit in place I also added a slot for a magnet at the bottom. This feature was problematic for several reasons:
- **Problem 1:** The magnets I was planing to use where not strong enough to hold the bit in place during some very scientific shake testing.
- **Problem 2:** I realized that having an exposed screw bit is quite dangerous and has high piercing potential for any storage container. Thus ideally I would add a cap to conceal the bit.
  I am not a big fan of pen caps since they add an additional element to keep track of and they are historically one of the most easy things to lose.
- **Problem 3:** I am already concerned about the structural integrity of the barrel without taking into account any twisting forces.

These problems would suppose a significant increase in the amount of work and complexity of this design, only to add an arguably useless feature. Thus I have decided to put aside this feature for the foreseeable future, whilst I perfect the main design.
### The clip
The clip of a pen is a very interesting and overlooked part of the pen, since it needs to be flexible enough without permanently deforming or snapping. For the clip to be 3D printed there was 2 options. Either it would be printed as a second part and then mounted onto the barrel, or it would be printed as one piece with the barrel. I did not like any of these options.

Printing it separately would allow for higher strength since the print layers would run along a longer plane instead of the shorter one. But it would also add more complexity, since it would involve at least 2 additional pieces for not that big of a benefit, since PLA is quite brittle and it would have snapped eventually.

Printing the clip as part of the barrel would reduce the complexity at the price of structural integrity. I was considering printing the barrel on its side as described in the section about the [structural integrity](#structural-integrity) but I was trying to avoid that solution since it would lead to an irregular surface finish.

This is when I remembered the Craighill [video](https://youtu.be/bFDt3lUzVPc?si=h_SgnaeWsf3YL5ZR) where they show how wire springs are a great compromise of form and function in carabiners and how they are a great option for pen clips. This is predominantly due to its great range of motion without risking plastic deformation.

Therefore I decided to make a rectangular lug on the side of the barrel with two holes. Then I deformed a paper clip into the desired shape. This version had 2 main problems. First, paperclips are famously deformable and thus it did not keep its shape during tests. Second, the clip would constantly slide out of the holes.
The first problem has an easy solution by choosing a stiffer wire. The second problem was not so obvious to solve. There was the option of a stiffer material preventing the clip from sliding out, but I was not so confident in this option. Thus I considered to make the holes tighter or longer.

Making the holes tighter would reduce lateral motion at the expense of potentially preventing the mechanism from working. This is because this wire is a great clip because when lifting it the wire will rotate in the whole misalignment the two arms which introduces rotational force making the wire act as a spring with only one loop (this is explained in further detail and better in Craighill's video, please check it out). A fundamental part of that mechanism is the wire being able to spin in the hole, thus making it tighter would potentially make it less effective.
Making the holes longer would also reduce the range of lateral motion, since the wire will "hit" the edge of the hole sooner, and it would not compromise the rotation.

Making the hole longer would make the lug wider which could look awkward. Since I was already considering removing the screwdriver I could also remove the lug and making the holes for the wire directly into the barrel, maximizing the length of the holes in the process. This was the final nail in the coffin to including a screwdriver bit into the pen. Not only did its addition add many problems but its removal would make this other more important feature a lot better.
## What can we improve on?
We have taken a very close look at all elements of Version one, the key takeaways from version 1 that I should try to implement into version 2 are:
- Design a more reliable tip attachment
- Mirror the design for a right handed version
- Test other geometries and textures to increase the grip of the barrel
- Compare strength and looks of different orientations
- Try other wire materials and place the holes in the barrel
# Version 2 (October 2026)
Version 2 was amazing, most of the issues of Version 1 were fixed and the current flaws are small enough that I am willing to call the project complete. 
But let us go over what these changes are and what new areas of improvement are.

<img src="https://edwasa.github.io/Articles/001_Ergonomic_Pen/Media/screw.jpeg" style="width: 350px">

## The tip
In order to make the screw thread properly I scaled the barrel up by 10% in the x and y axis (note not the z axis since this would mess with the thread spacing). This simple fix solved all of my issues with the thread in the first version.
The scaling lead to an awkward step between the tip and the barrel (because they where no longer the same diameter), hence I made the tip larger by 10% without affecting the screw part.

Another quality of life improvement I did was make the screw shorter since my screw twice as long as the ones in other pens I had at home (10mm vs 5mm), this made screwing the tip less tedious when replacing the ink.
## The barrel
In order to improve the holding experience I have replaced the cylindrical shaft for a hexagonal one (just like in pencils). This significantly improved the holding experience and stops the pen from rolling away even more.


On the topic of improving grip, I also tried out CNC Kitchens tool for adding textures to 3D prints and I have gotten mixed results. The grip did certainly improve but I got mixed responses for the looks. Some users preferred it while others considered it ugly. Thus I will provide both versions and possibly experiment with more subtle textures too.

I performed the stress test (I tried to snap the pen in half) on the first version and it snapped as expected. In order to increase structural integrity of the pen I tried printing the shaft on its side, which made it stronger. But since the pen is now hexagonal all the faces had different and very rough textures, which was a bit of an eye sore. 
I have been carrying this pen on my back pocket for a few weeks, during which I have sat on it numerous times and it has not snapped with the vertical (and weaker) printing orientation. Thus I have decided that for aesthetic reasons I will choose the prettier but less strong printing orientation, since the pen so far appears to be strong enough for regular everyday use.
## The Butt
As discussed in the first version I have decided to remove the screwdriver bit for good.

As for the clip I bought thicker and stronger wire and it has given better results. The wire might be a bit thin since it can still deform when opening the clip further than 90 degrees, but this is already further than commercially available pens.

Making the wire straight was difficult at first, but I have found this jewelers trick to make wire straight. It consists of holding the wire with a towel and puling the wire between your fingers at a 90 degree angle. If you repeat this process enough times and change the direction of the bend each time the wire will become straight.
# Conclusion
I am very happy with the resulting product and I have been using it on a daily basis for the past few weeks. It brings me joy to use it since it really is much more ergonomic than normal ballpoint pens.

The issues from V2 are small enough that they do not bother me, but in case of mass production could be fixed relatively easily by choosing other materials and production methods.

I will be uploading the files to printables and maker world in case you want to make your own ergonomic bolt action pen. As additional materials you will need an ink cartridge with the wings, a pen spring and an M2 bolt for the pin.

---
Article by Eduard Wagener

15th of October 2026
# Links
- Inspiration pen in maker world --> https://makerworld.com/models/1440290?appSharePlatform=copy
- Video about retractable mechanism --> https://youtu.be/Zv5Qa2kGL04?si=GeoqBJl5t0IR3pbY
- Scott Russel linkage --> https://en.wikipedia.org/wiki/Scott_Russell_linkage
- Printables --> TBD
- Maker world --> TBD
- Bump mesh --> https://bumpmesh.com/
- Craighill video --> https://youtu.be/bFDt3lUzVPc?si=h_SgnaeWsf3YL5ZR