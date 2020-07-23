# Do-it-yourself: Smart IKEA EVEDAL

Recently while shopping at IKEA, I saw a table lamp which look great à 30$ instead of 200$ CAD. The only thing is that it was a dumb lamp, while all light in my house are now smart.
![00-Original](assets/00-Original.jpg "00-Original")

So here is my work to make it a bit smarter!

> Note: For this original work, I only replaced the bulb socket by a standard E26. 
> The slider switch is no longer usable.
> I plan to reuse it using an ESP-8266, but it's not part of this work!

## Material
* A smart bulb **with plastic cap** (cf. point 18 and 19) eg. [Inovelli Ilumin](https://inovelli.com/products/bulbs-ilumin/) or [IKEA TRADFRI](https://www.ikea.com/ca/en/p/tradfri-led-bulb-e26-600-lumen-wireless-dimmable-color-and-white-spectrum-color-and-white-spectrum-globe-opal-white-90408617/);
* A [bulb socket](https://www.homedepot.ca/product/atron-porcelain-socket-with-leads/1000424526);
* A 1/4 x 1.5-inch bolt;
* Basic tools!

## Step by step
1.	The first step is to remove the LED bulb, you only have to pull it

	![01-RemoveBulb](assets/01-RemoveBulb.jpg "01-RemoveBulb")

2.	Then we have to remove the switch. It’s only screwed in the lamp’s base, but it’s a bit hard to unscrew it. I used a pliers with piece of plastic warp to protect the slider.

	![02-RemoveSwitch.1](assets/02-RemoveSwitch.1.jpg "02-RemoveSwitch.1")

	![02-RemoveSwitch.2](assets/02-RemoveSwitch.2.jpg "02-RemoveSwitch.2")

	![02-RemoveSwitch.3](assets/02-RemoveSwitch.3.jpg "02-RemoveSwitch.3")

3.	Next step is to remove the bottom pad with a cutter

	![03-RemoveBottom.1](assets/03-RemoveBottom.1.jpg "03-RemoveBottom.1")
	
	![03-RemoveBottom.2](assets/03-RemoveBottom.2.jpg "03-RemoveBottom.2")
	
	![03-RemoveBottom.3](assets/03-RemoveBottom.3.jpg "03-RemoveBottom.3")

4.	To dismount the base, you need to give more cable by pushing it inside, then you only have to pull it from the bottom.

	![04-DismountBase.1](assets/04-DismountBase.1.jpg "04-DismountBase.1")

	> Note: On the first lamp I modified, the cable was locked by a small clip on the side
	>
	> ![04-DismountBase.2](assets/04-DismountBase.2.jpg "04-DismountBase.2")
	> *	Push the cable from outside in the base;
	> *	Using a screwdriver, pull the cable above the clip to give enough space to remove it;
	> *	Remove this clip;
	> *	Then push back the cable inside

	![04-DismountBase.3](assets/04-DismountBase.3.jpg "04-DismountBase.3")

	![04-DismountBase.4](assets/04-DismountBase.4.jpg "04-DismountBase.4")

5.	Unplug the power adapter and cut the 2 wires that are going through the base to the top of the light

	![05-CutWires](assets/05-CutWires.jpg "05-CutWires")

6.	Unscrew the plastic nut, and dismount the plate on top

	![06-DismountBuldSupport.1](assets/06-DismountBuldSupport.1.jpg "06-DismountBuldSupport.1")

	![06-DismountBuldSupport.2](assets/06-DismountBuldSupport.2.jpg "06-DismountBuldSupport.2")

7.	Unscrew the two small screws on the side of the bulb socket and pull it off

	![07-RemoveBulbSupport.1](assets/07-RemoveBulbSupport.1.jpg "07-RemoveBulbSupport.1")

	![07-RemoveBulbSupport.2](assets/07-RemoveBulbSupport.2.jpg "07-RemoveBulbSupport.2")

8.	Drill 2 holes in the plate to pass the new wires

	![08-PrepareSupport](assets/08-PrepareSupport.jpg "08-PrepareSupport")

9.	Now it’s time to mount the new bulb socket!

	The main issue here is that it usually comes ready to be mounted on a classic lamp thread, which we don’t have and would be harder to fit.

	![09-AdaptNewSocket.1](assets/09-AdaptNewSocket.1.jpg "09-AdaptNewSocket.1")

	Instead, I unscrew the small support under the socket, and using some pliers I “reversed” it to fit in the hole of the plastic plate of the lamp.

	![09-AdaptNewSocket.2](assets/09-AdaptNewSocket.2.jpg "09-AdaptNewSocket.2")

10.	Mount the reversed support using the bolt on the plastic plate

	![10-MountSocketSupport](assets/10-MountSocketSupport.jpg "10-MountSocketSupport")

11.	And finally fix the new socket on the support

	![11-MountSocket](assets/11-MountSocket.jpg "11-MountSocket")

12.	Using the plastic nut, screw it back to the base of the lamp

	![12-ReplaceSupport](assets/12-ReplaceSupport.jpg "12-ReplaceSupport")

13.	Time to wire it! Cut the plastic protection and dismount the electrical connector

	![13-ElectricalConnector.1](assets/13-ElectricalConnector.1.jpg "13-ElectricalConnector.1")

	![13-ElectricalConnector.2](assets/13-ElectricalConnector.2.jpg "13-ElectricalConnector.2")

14.	Connect the 2 wires of the socket, put back the connector (or use new one!), and wrap it in electrical tape

	![14-Connect](assets/14-Connect.jpg "14-Connect")

15.	Push everything back into the base

	> Note: Here I kept the power adapter but disconnected it (I moved the power connector in whole on the side). The idea (for a next how-to) will be to use a small ESP8266 to re-use the original switch to control the lamp.

	![15-BackIn](assets/15-BackIn.jpg "15-BackIn")

16.	Screw back the switch and make sure that everything is well aligned (move the slider up and down, manipulation should be smooth).

	![16-PutBackSwitch](assets/16-PutBackSwitch.jpg "16-PutBackSwitch")

17.	Screw the smart bulb and plug the lamp in the wall to validate that everything is ok.

	![17-PutBackBottomPad](assets/17-PutBackBottomPad.jpg "17-PutBackBottomPad")

18.	The surprise steps … all bulbs I’ve tested (Phillips Hue, IKEA TRÅDFRI, and Innovelli Ilumin) are slightly to big to fit in the lamp 😣. So we have to remove the cap of the bulb!

	![18-FitBulb](assets/18-FitBulb.jpg "18-FitBulb")

19.	Using a cutter, either cut (IKEA TRÅDFRI) or separate (Innovelli Ilumin) the cap of the bulb.

	> WARNING: Make sure the cap of the bulb is in plastic! Apparently, it’s in glass for the Phillips Hue, so I didn’t tried!

	![19-RemoveCap.1](assets/19-RemoveCap.1.jpg "19-RemoveCap.1")

	![19-RemoveCap.2](assets/19-RemoveCap.2.jpg "19-RemoveCap.2")

	![19-RemoveCap.3](assets/19-RemoveCap.3.jpg "19-RemoveCap.3")

20.	Enjoy!

	![20-Enjoy.1](assets/20-Enjoy.1.jpg "20-Enjoy.1")

	![20-Enjoy.2](assets/20-Enjoy.2.jpg "20-Enjoy.2")

	![20-Enjoy.3](assets/20-Enjoy.3.jpg "20-Enjoy.3")






