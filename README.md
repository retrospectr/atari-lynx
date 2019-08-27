# Atari Lynx Fix
Hey, I fixed my faulty Atari Lynx I and documented everything on youtube. For those who have similar problems and want to fix their 
 handhelds, please feel free to use the schematics, pictures, circuits and explanations that could be found in this repository.
  
Since the power circuits of the Lynx I and the Lynx II are similar, this repository might be useful for both versions. 
  
Structure of this repo:  
  

* [schematics](./schematics) usefull schematics for Lynx I and Lynx II
* [pics](./pics) pictures I made from the PCB of my Lynx (version 1)
* [slides](./slides) explanations where to find components on the pcb, etc..


## What is an Atari Lynx?
The Lynx was the world's first handheld color video game system released in 1989. This was the same year when Nintendo released 
the successful GameBoy and one year before Sega followed with the Game Gear. 


## What was faulty?
My Lynx did not power up. It does nothing when pressing the power button. When I connect 5 Volts but put Ground
to ```L6```, the system powers up properly. Thus, the handheld by itself was working and the issue was located in the power circuit itself. 


## Things I've done

I thought that the MOSFET might be faulty so I searched online for a replacement. By searching for the part number ```MTD 3055``` i found many results dealing with the Atari Lynx Power Problem. 
 One of the first results where a complete replacement kit at [Console 5](https://console5.com/store/catalogsearch/result/?q=atari+lynx) for a reasable price. So i ordered and replaced 
 the transistors ```Q4``` and ```Q13```, the Zener Diode ```ZD1``` and the MOSFET ```Q11``` (for Lynx II : ```Q7```,```Q8```, ```D13```, ```Q12```)

But, that does not do the trick. The Lynx still won't turn on. I measured all resistors and checked all traces of the power circuit for continuity. 
I also measured connection points when powering up in order to determine which component might be faulty. 
Additionally, I changed all electrolytic capacitors (even there was no sign of leakage). 


## Where are components located on the board?

I prepared a few [slides](./slides/power_circuit.pptx) that show you where the main components are located on the PCB (Lynx I only). 


## Test circuits with iCircuit

I made use of the software [iCircuit](http://icircuitapp.com/) to simulate the power circuit of the Lynx. It helped me a lot
 to understand the functionality while playing around. In the video, I tried to explain
 how the voltage regulation works with MOSFET and Zener Diodes (or at least how I believe it works).
  
The following files might help you:

* [digital_relais.icircuit](./schematics/digital_relais.icircuit) demonstrates how to power up things with a single button press
* [voltage_divider_with_zener.icircuit](schematics/voltage_divider_with_zener.icircuit) demonstrates the usage of a Zener diode as voltage divider
* [power_up.icircuit](./schematics/power_up.icircuit) The complete power circuit of the Lynx (I and II are similar). It does not react like the real one, because parameters for MOSFET, transistors and Zener diode are not matching  



# Useful links

* [Console 5](https://console5.com/store/catalogsearch/result/?q=atari+lynx)
* [Lynx schematics at Atariage](https://atariage.com/Lynx/archives/schematics/index.html?SystemID=LYNX)
* [Developers Documentation](https://atariage.com/Lynx/archives/developer_docs/LynxDeveloperDocs.zip)