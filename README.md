# 12AU7-Headphone-Amplifier
Headphone amplifier with 12AU7 preamp section. Based from the Bravo Audio V2 amplifier.

I've been using a Bravo Audio V2 headphone amplifier for probably ten years now. The build quality is bad and it's a miricle that it has lasted just this long. It's had multiple reapirs, modifications and heavy use for the whole time. I went to find a new one and they have since disapeared from the internet. Well, perfect excuse to build a replica where cost is not an issue.

This is a replica of how my own amplifier is currently working. This V1 is to confirm I can actually build the thing and have something that works. It is as yet untested in this state. I've designed it to use the power supply from my existing unit. The modifications made to this are: better quality output MOSFETs, better quality current regulators, a better choice of input capacitor value, removal of useless bridge between valve heaters, larger regulator heatsink and removal of parts I never use.

![PCB Layout](https://github.com/sillyhatday/12AU7-Headphone-Amplifier/assets/65309612/d4de6558-2ef3-41cd-b668-5a8d6f326350)
![Bravo Amp Rep Top](https://github.com/sillyhatday/12AU7-Headphone-Amplifier/assets/65309612/d68e6092-f0fb-495e-a719-ad50b6a6dc84)
![Bravo Amp Rep Bottom](https://github.com/sillyhatday/12AU7-Headphone-Amplifier/assets/65309612/eceb9893-a6e5-479f-bf10-6b5299db69b0)
![Bravo Amp Rep Angle2](https://github.com/sillyhatday/12AU7-Headphone-Amplifier/assets/65309612/711ed6f2-f39f-495b-8bcb-1b95dfd24dcc)


General Information on the original amplifer:

TO BE FILLED

Bill of Materials:
| Part | Quantity |
|---|---|
| DC Jack DCJ200-10-A-K1-K | 1 |
| Aliexpress Heatsinks 25x23x16 TO220 | 4 |
| RCA Jack 36-901-ND | 2 |
| Aliexpress Valve Socket 9-Pin | 1 |
| Neutrik 1/4" PCB Jack NMJ6HFD2 | 1 |
| IRL530 Mosfet | 2 |
| LM317A | 2 |
| 12AU7/ECC83 | 1 |
| RED Strawhat LED | 1 |
| Pot ALPS RK097 10K | 1 |
| 2N3906 PNP Transistor | 2 |
| Resistor 47K | 2 |
| Resistor 24K | 2 |
| Resistor 10K | 1 |
| Resistor 3K | 4 |
| Resistor 220R | 2 |
| Resistor 7R5 | 2 |
| Capacitor 6800uF | 1 |
| Capacitor 1000uF | 2 |
| Capacitor 2.2uF | 2 |
| Capacitor 100nF | 2 |

Future revisions:

Once proven to be a working amplifer, I would like to make many more serious modifications. The best way is to do them one at a time to allow easier troubleshooting if required.

Add some power filtering such as a choke or some inductor. I need to learn more about the effects of this, what is best and how to calculate it.

First major modification I would like to do is remove the valve heaters from the audio signal path. This helps with sound quality as it causes crosstalk between channels. This will require much larger heat sinks for the current regulators as they will have to deal with an extra 6.3v. Along with a seperate 6.3v power supply for the heaters wither on the bard regulating 24v down to 6.3v or completely seperate.

In general I would like to use bigger heatsinks on everything to keep things much cooler. The standard heatsinks are a burn hazard. They run very hot. This has not proven to be an issue with reliability.

Do more work on laying out the board to keep each channel sepereated as best as possible, also keep input and output signal paths sepereated. Need to learn more about PCB design to improve this.

Adjustable output resistor for impedance matching headphones. This should be a simple mod by adding another dual wipe pot along side the volume control pot.

Input gain switch. Probably add a selectable resistor to the input volume pot to tame the volume. You bearly have to turn this thing 45 degrees from 0 and it blows out your ears. More control of the dial would be better while allowing it to be switched out to run higher impedance headphones. This will also allow you to comensate for running higher output impedance values by allowing more input signal in and lower output values you can switch in a higher resistance.

Adjustable plate voltage would also be a great option for using different valves. In general the low voltage being used isn't optimal for the valve as it is but adding more flexibility can't be a bad option.

Higher running voltage. This will probably be the hardest to implement. It most probably will not work with this design or require many parrallel parts to distribute extra power losses. This will also make the size much much bigger than before. Probably double the voltage to 48v and quadruple the amount of MOSFETS and different current regulation.

Findout truely what the fuck the two small transistors are that feed the valve anode. I have looked at all kinds of things from constant current sources and current mirrors. I don't se why they are even needed, but as the orginal chinese design used them while cuttings costs everywhere, they must be needed.

Is it possible to create a true balanced headphone output. I need to learn much more about amplifer design and the workings of balanced amplifers to do this. It might not even be possible with this design.

Using of different valves from the family like a 12AX7 and 12AT7. Again my not be possible to make anything good but worth a look at.
