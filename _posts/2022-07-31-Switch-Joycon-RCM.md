---
layout: post
title: JoyCon RCM Jig
image:  /images/posts/joycon-thumb.jpg
tags:   hacking
excerpt: Adding an RCM jig inside a Nintendo Joycon.
---

## Rationale
Entering RCM mode involves shorting (connecting) two pins on the Switch's joy con rail. A typical jig is a piece of plastic which slides into the rail and aligns a piece of wire to connect the pins.

Instead of using a separate jig, we can short the pins inside the joycon controller while it's still attached, by connecting the shorting circuit to an external button. In this case, we use the joycon's `rail release` button as it's not wired into an existing circuit.

Once completed, RCM mode can be entered by holding the `Vol+` and `release` button during a reboot.

## Required
- Metal Joycon buckle lock (see picture -- found on [AliExpress](https://www.aliexpress.com/wholesale?catId=0&SearchText=nintendo+switch+metal+lock) or [eBay](https://www.ebay.co.uk/sch/i.html?_nkw=nintendo+switch+metal+lock))
- Stranded wire
- Sticky tape
- Soldering iron
- Screwdrivers -- phillips head and Nintendo tri wing

<img src="/images/posts/joycon-buckle-locks.png" alt="Joycon buckle locks" width="400"/>

## Process
The first task is to open the right joycon controller and remove the rail mount. The instructions for this can be found on other sites (e.g. [iFixit](https://www.ifixit.com/Guide/Joy-Con+Buckle+Lock+Replacement/103997)) and are not repeated here.

Once the rail is removed, the pin breakouts can be seen on the bottom of the rail. We need to connect two of these pins (7 and 10) to the physical button at the other end of the rail.

<img src="/images/posts/joycon-pins.jpg" alt="Joycon pins" width="600"/>

Two wires are soldered to the back sides of pins 7 and 10 and run along the rail's board. As the internals of the joycon case are tightly-fit, sheathed wires are difficult to find spare for. Therefore, a stranded wire is stripped and two strands used -- be careful that the paths used for these wires do not connect to other metal areas and create shorts. The wires can be seen in the picture of the completed installation below and are highlighted in the adjacent picture. Note the extra slack in the right (green) wire to allow for the travel of the button.

<table><tr>
  <td>
    <img src="/images/posts/joycon-completed.jpg" alt="Joycon with wires installed" width="600"/>
  </td>
  <td>&nbsp;</td>
  <td>
    <img src="/images/posts/joycon-wires.jpg" alt="Joycon with wires installed -- highlighted" width="600"/>
  </td>
</tr></table>

The plastic buckle lock is replaced with the metal buckle. At rest, the metal buckle does not touch the metal bracket above it, but as the button is pressed, a connection is made. Therefore we can connect the wire ends these components. The wire on the buckle lock is soldered to the 'top' of the piece (see picture below). Make sure there is enough slack in the wire to allow for the required range of motion.

<img src="/images/posts/joycon-solder.jpg" alt="Wire soldered to buckle lock" width="600"/>

The other wire can be connected to the bracket without solder -- simply create a loop at the end of the wire for the screw to pass through and place it between the buckle and the plastic rail.

<img src="/images/posts/joycon-wire-loop.jpg" alt="Wire loop for screw mount" width="600"/>

Before replacing the buckle over the wire loop, we add some circuit protection -- because the rail is fixed rigidly to the switch but the joycons are sometimes flexed during play, the components inside the joycon sometimes apply pressure to the bracket and push it down onto the lock, completing the circuit. When using the Switch, this will manifest as the controller disconnecting until a few seconds after the pressure is released. Therefore, a small piece of sticky tape is applied underneath the bracket to prevent this electrical connection. The buckle therefore makes contact on the side of the bracket (i.e. only when pressed). Be careful that the tape does not wrap around to cover the bracket edge used for this connection. There's a small upward lip on the bracket used for the connection -- see the diagram.

<table><tr>
  <td>
    <img src="/images/posts/joycon-buckle-tape.jpg" alt="Tape applied to buckle" width="400"/></td>
  <td>&nbsp;</td>
  <td>
    <img src="/images/posts/joycon-diagram.jpg" alt="Joycon diagram for tape application" width="400"/>
  </td>
</tr></table>

If you have a multimeter, you can now check that the connections are working correctly in both states -- at rest and when the button is pressed.

When restarting the Switch, holding the `Vol+` and modified `rail release` buttons will boot the Switch in *RCM mode*. When successful, the screen will not power on, but the RCM state can be verified by testing whether an injector detects the device. For example, connect the Switch to a computer via USB and try the injection on [this site](https://switch.exploit.fortheusers.org/) (must use Google Chrome). The Switch should appear as a device called `APX`. Note that some USB cables are used for charging and don't transmit data, in which case they won't work for this. If the device doesn't appear, try a few different cables.

Note that jailbreaking the device requires additional steps to prepare an SD card, and are not covered here.

## References
- This build is an extension of an idea from Discord user pbanj#9188 on the [Nintendo Homebrew Discord Server](https://discord.com/invite/C29hYvh)
- A guide on jailbreaking the Switch can be found [here](https://rentry.org/SwitchHackingIsEasy).
