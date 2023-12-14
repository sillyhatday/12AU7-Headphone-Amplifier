## Preface
If you are looking for a serious project then this is not for you. It is based on a flawed design with easy improvements. Go buy something that is proven to sound good. This is not it. That said you will have something perfectly listenable and a cheap entry point to vacuum tube amplification.

## 12AU7-Headphone-Amplifier

Headphone amplifier with 12AU7 preamp section. Based from the Bravo Audio V2 amplifier.

I've been using a Bravo Audio V2 headphone amplifier on and off for probably ten years now. The build quality is bad and it's a miracle that it has lasted just this long. It's had multiple repairs, modifications and heavy use for the whole time. I went to find a new one and they have since disappeared from the internet. Well, perfect excuse to build a replica where cost is not an issue.

I've designed it to use the power supply from my existing unit. The modifications made to this are: better quality output MOSFETs, better quality current regulators, a better choice of input capacitor value, better choice of input capacitor type, removal of useless bridge between valve heaters, larger regulator heatsink, adjustable anode bias and removal of the awful blue LED.

![Bravo Amp Rep V1 2](https://github.com/sillyhatday/12AU7-Headphone-Amplifier/assets/65309612/0c12abed-224b-4746-88f3-91b910cedec0)
![WhatsApp Image 2023-11-28 at 17 54 07_dc16360e](https://github.com/sillyhatday/12AU7-Headphone-Amplifier/assets/65309612/ac1c4b83-45c0-4f2f-81c2-c8712ad9e2e9)

## General Information on the original amplifier:

The whole base of this project was this little amplifier that could. It seemed more of a curiosity or a gateway to higher level vacuum tube amplifiers, from around 2013 onwards. I found it fascinating. Working from memory, this small curiosity actually seemed to get some praise. There was a lot of cheap Chinese valve amplifiers on sale at this time and it seemed like a lot of them were complete trash or didn't even use the vacuum tube. This was the cheapest vacuum tube headphone amp around at the time. I don't know if there is a replacement for this by someone else these days; I feel that it's legacy should live on.

Many of the more invested audio geeks will say it sound bad. That is unfair. It does not sound bad at all, in fact it sounds good. I think everyone has heard bad sounding audio equipment, they know how bad it sounds. The threshold of sounding good, doesn't change based on how much better higher level equipment sounds. Justification for your high level spending changes the threshold of good sound for yourself. There are better things out there of course. At the time this thing with some small modifications could compete with amplifiers and 4 times the price (based on what I've read).

So why not carry on the legacy of an absolute entry level vacuum tube headphone amplifier. Even with the cost of high quality components, the cost of this isn't far beyond the price of these things originally. I think they were around £60 at the cheapest. With all parts needed and the PCB it isn't far off. The included Chinese vacuum tube wasn't great. Changing the included vacuum tube is a solid improvement.  The idea of the best sounding tube is a whole story in itself, therefore it is up to you to decide what is best. You shouldn't discount the cheap tube ones, you can find something that sounds good to you. Different genres of music match other tubes better. Over the years I settled on a Brimar 12AU7, that was brand new from someone I knew.

5963 tubes are, or were, the cheapest option. Philips 5963 is probably the worst I have heard, it is detailed and clear sounding, a nice sound all around. The problem is it sounds like all sound is coming from one place. It doesn’t sound bad as such. They are so cheap it is worth getting one to play around with.
The RCA 5963 sounds a little warmer than that. It has a much more open sound and the magic you want from a tube amp. Super airy open soundstage, beyond anything I’ve heard with headphones before. Details that I’ve not heard before come out naturally. Well recorded drums, the cymbols don’t just have that usual sound but you can hear the metal resonate. Magical. The downside is it does loose some low end. It’s more suited to something like Jazz where the details really make the music.
The Brimar 12AU7 is where it is at. It looses detail over the other two but doesn't sound muffled. It smooths out the midrange while not pushing it back. The low end gains a butter smooth clarity and a boost over the RCA Grey plate. The whole sound is coloured by a warm tone. It sounds great with rock and metal where the brittle sounding guitars have the edge taken away and meld into thick soup without loosing the individual details.

I hope that anyone who wants to experiment with vacuum tubes can find some enjoyment from this project. It doesn't have to be an expensive hobby. It should be something that is fun and within your budget. If you can't afford the best stuff out there, then don't worry, there are a lot of cheap options out there like this little amplifier that could.

![Bravo-Audio-V2-Class-A-12AU7-Tube-Multi-Hybrid-Headphone-Amplifier-Listen-to-Better-Music-2219735662](https://github.com/sillyhatday/12AU7-Headphone-Amplifier/assets/65309612/a616416b-b9f8-4374-bb6d-3059405e4e6e)


# Bill of Materials:
| Part | Quantity |
|---|---|
| DC Jack DCJ200-10-A-K1-K | 1 |
| Aliexpress Heatsinks 25x23x16 TO220 | 4 |
| RCA Jack 36-901-ND | 2 |
| Aliexpress Valve Socket 9-Pin | 1 |
| Neutrik 1/4" PCB Jack NMJ6HFD2 | 1 |
| IRL510/IRL530/IRF510/IRF530/IRF630 Mosfet | 2 |
| LM317A | 2 |
| 12AU7/ECC82 | 1 |
| RED Strawhat LED | 1 |
| Pot ALPS RK097 10K | 1 |
| 2N3906 PNP Transistor | 2 |
| Resistor 47K | 2 |
| Resistor 24K | 2 |
| Resistor 10K | 1 |
| Resistor 3K | 4 |
| Resistor 220R | 2 |
| Resistor 7R5 | 2 |
| Electrolytic Capacitor 6800uF 35v | 1 |
| Electrolytic Capacitor 2200uF 35v | 2 |
| Film Capacitor 2.2uF 50v | 2 |
| Ceramic Capacitor 100nF | 2 |

![Footprint notes](https://github.com/sillyhatday/12AU7-Headphone-Amplifier/assets/65309612/7611e690-aa84-47bd-85c4-8689cdeca6ff)

### Notes:

You can choose freely as to which MOSFET to use in the amplifier. The best ones are the IRL series. I think the IRF should still sound very good indeed. Avoid the IRF630 unless you like a slow filtered roll off above 10kHz. The input capacitance is brutal. You might like that sound and it is the cheapest one so feel free to experiment.
Valve choice is really what this is all about. There are huge differences in sound between them. Some more than others. Then you also have other ranges of valve that are similar to the 12AU7. I have only tested the 5963 but here are some other types that should work too: 6189, 5963, 12AX7, 12AT7, 5814 and more when I find my notes.

## Information on the design:

### Bias control resistors:

A major flaw in the original design of this amp was the poorly calculated (or not calculated) bias for the 12AU7 anode. I have not done any measurements on the original amplifier, but I took measurements on the prototype of this newly built amplifier using the same value parts as the original. The 12AU7 needs a constant current following through the anode. The small PNP transistors are setup as a constant current source for this purpose. The current flow being used is only a few hundred uA. I’ve not looked into the optimal current to use yet for a 12AU7 but as the whole thing is being run from 24v the tube is working well outside it’s optimal setting to begin with.
The constant current flowing through the valve is affected by the signal input to the grid. The changing voltage on the grid tries its best to change the current flowing through the 12AU7. The constant current source fights back and adjust the voltage on the anode to keep the current constant. This changing voltage on the anode is fed into the MOSFET stage.

To properly set the bias without a target number, you just need to play it by ear, literally. Just go with what setting sounds best to you, while keeping the anode current as low as possible as this will increase the idle current through the MOSFET stage, creating more heat. The heatsink size is already at its limit for the MOSFETs. If higher anode current is needed, I suggest using larger heatsinks on the MOSFETs. These cheap heatsinks should be able to stack. Put a small film of thermal paste on the top of the heatsink and force the pins on the bottom of another into the channels on the top of the first. Alternatively, there are some slightly taller versions.
The actual setting of the bias, in reality, is not so easy to set by measuring current. Due to ohms law though we know current can be changed by changing resistance or voltage. With the amplifier in a steady idle state, measure the voltage on the test points TP1 to TP3 and TP2 to TP3. The voltage will vary depending on the 12AU7 being used. I find most of them to be similar. The factory values for the bias had the anode below 10v, which does work, but an extra volt on every valve I tried makes a huge difference in sound quality. I’ve found 10.5 to 10.8v on all the valves I tried to be the minimum voltage before loosing sound quality. Anything higher just seems to be wasted energy and extra heat.
The range of settings available are larger enough to be more than needed without causing damage to anything if used only for a short period. I can’t guarantee that the highest current setting will not boil your 12AU7 and output MOSFETs.

### Output impedance:

I’ve played around with this setting by experimenting blind and it also makes a big difference. The simple answer is to make it as low as possible and forget about it.
There are plenty of information sources about amplifier output impedance, so I’ll not repeat in here. Basically the lower the better. High output impedance changes your headphones character, usually for the worse. I left the resistor in place to add some output impedance in case someone wanted to play around and adjust it to purposely change the headphones character.
The original design had a 47R resistor in place, which makes zero sense. Any headphones with a 32ohm impedance sound like trash. You need at least 376ohm headphones to get to the sweet spot. The only reason I see for the high output impedance is that this amplifier design is trash. With a low value resistor and sensitive headphones the background hiss is unbearable in an idle state. I think it was done to hide the background hiss as best as they could.
Experiment and find out what sounds best to you.

### Input capacitors:

The original design once more used less than ideal components. The choice of 1uf was decent enough but caused a bass roll off in the sub bass region and as the higher bass frequencies are in the space where this filtering effect happens, it causes phasing issues with those frequencies. Once more affecting the sound quality. Changing to 2.2uf moves the filter even lower and well out of the way. They are not needed at all if your source connected to the input has no DC bias on it. Any of that will affect the sound quality and/or throw the tube into a run away.
The other issue is the type of capacitor used. The original used electrolytic type. The problem with this is the input has no DC bias on either side of it. So with AC source input you are running the capacitor into reverse bias. It’s well within the tolerance limits but it still uses the capacitor in a non optimal way. So 2.2uf film capacitors are used instead. The bass should be cleaner and possibly sound better over all using a more suitable capacitor type.

## Final thoughts:

I made a list at the start of this project of my thoughts about future improvements. I don’t think it is really worth adding so many large changes into this design. It sounds pretty good as it stands now.

To continue changing this design is missing the point of it. It was to create a cheap vacuum tube amplifier from an existing flawed design to have fun with. No amount of tweaking forever will improve things much more (With one exception) than this. It’s worth putting the time into a fresh new design, based on knowledge gained from this project. I did my best to reverse engineer this to learn. Nothing I’ve done was without knowing how it works.

To the one exception is the removal of the valve heaters from the current path of the MOSFETs. That is still worth doing. It will require a board redesign for extra components and the huge heatsinks it will require on the LM317s. I’ll make that a separate project and call it the plus version of this or something.
After that I feel like starting something else like this completely from scratch. That will take some time.

I think I have accomplished what I set out to do. I had fun and created something usable. As a bonus it also sounds better than I thought it ever would. Happy listening.

## Changelog:

### Changes from version 1.1 to version 1.2 are as follows:

Added valve anode bias adjustment pots with limiting resistor and test points for easier bias setting.

Added 3.5mm input and output jacks for extra flexibility.

Changed valve socket footprint to fit the socket better.

Changed heatsink footprint to actually fit the heatsink. The provided diagrams were not even close to reality.

Changed audio input capacitors to a more suitable type. May improve sound quality, maybe not.

Removed a 100nF filter capacitor. The remaining one is a token gesture.

Changed output resistor to low value for better impedance matching.

### Changes from version 1 to version 1.1 are as follows:

Capacitor silk screen orientation corrected. Used wrong symbols in the schematic and it caused the footprint to be totally random.

Volume potentiometer wired weird. I could have caught this but I didn't. Schematic symbol not very clear honestly.

Volume potentiometer position moved slightly.

TO220 packages moved slightly closer to heatsinks.

Headphone output footprint backwards. Impossible to know without having the component to look at and reference to the footprint.

Swapped the left and right input caps to actually be on the left and right. Why I crossed them over I don't know. Makes no difference, I just like to have left on the left and rightr on the right.

Added L and R to input jack footprint. If not using colour coded jacks you can tell the difference. If using colour coded jacks you can see which to put where.

# Future revisions:

*No longer plan to do any more with this design and just move onto something new*

USB-C power supply. It can be done. How complex it may be, I do not know. This needs 24v and max USB-C power is 20v? I'm not sure, but it would be a very nice additon. A nice linear regulated power supply would be best, but this is a cheap fun toy.

Add some power filtering such as a choke or some inductor. I need to learn more about the effects of this, what is best and how to calculate it.

First major modification I would like to do is remove the valve heaters from the audio signal path. This helps with sound quality as it causes crosstalk between channels. This will require much larger heat sinks for the current regulators as they will have to deal with an extra 6.3v. Along with a separate 6.3v power supply for the heaters whether on the board regulating 24v down to 6.3v or completely separate.

In general I would like to use bigger heatsinks on everything to keep things much cooler. The standard heatsinks are a burn hazard. They run very hot. This has not proven to be an issue with reliability.

Do more work on laying out the board to keep each channel separated as best as possible, also keep input and output signal paths separated. Need to learn more about PCB design to improve this.

Input gain switch. Probably add a selectable resistor to the input volume pot to tame the volume. You barely have to turn this thing 45 degrees from 0 and it blows out your ears. More control of the dial would be better while allowing it to be switched out to run higher impedance headphones. This will also allow you to compensate for running higher output impedance values by allowing more input signal in and lower output values you can switch in a higher resistance.

Higher running voltage. This will probably be the hardest to implement. It most probably will not work with this design or require many parallel parts to distribute extra power losses. This will also make the size much much bigger than before. Probably double the voltage to 48v and quadruple the amount of MOSFETS and different current regulation.

Is it possible to create a true balanced headphone output. I need to learn much more about amplifier design and the workings of balanced amplifiers to do this. It might
 not even be possible with this design.

Using of different valves from the family like a 12AX7 and 12AT7. Again my not be possible to make anything good but worth a look at.
