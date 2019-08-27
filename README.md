# Atari Lynx Fix
Hey, I fixed my faulty Atari Lynx and documented everything on youtube. For those who have similar problems and want to fix their 
 handhelds, please feel free to use the schematics, pictures, circuits and explanations that could be found in this repository.
  
* [schematics](./schematics)
* [pics](./pics)
* [slides](./slides)


## What is an Atari Lynx?
The Lynx was the world's first handheld color video game system released in 1989. This was the same year when Nintendo released 
the successful GameBoy and one year before Sega followed with the Game Gear. 


## What was faulty?
My Lynx did not power up. It does nothing when pressing the power button. If i connect 5 Volts to VCC and Ground
to the MOSFET, it boots up properly. So the handheld by itself was working --> the issue was located in the power circuit itself. 


## Things I've done

- changed power components
- changed all electrolytik capacitors (even there was no sign of leakage)
- measured connection points when powering up
- changed all capacitors in power circle


### Test circuits with iCircuit

I made use of the software [iCircuit](http://icircuitapp.com/) to simulate the power circuit of the Lynx. It helped me a lot
 to understand the functionality and test around how the whole thing react when components are faulty. In the video, I tried to explain
 how the voltage regulation works with jFET and Zener Diodes (or atl least how I believe it works).
  
The following files might help you:

* [digital_relais.icircuit](./schematics/digital_relais.icircuit) demonstrates how to power up things with a single button press
* [voltage_divider_with_zener.icircuit](schematics/voltage_divider_with_zener.icircuit) demonstrates the usage of a Zener diode as voltage divider
* [power_up.icircuit](./schematics/power_up.icircuit) The complete power circuit of the Lynx. It does not react like the real one, parameters for jFET, transistors and Zener diode are not matching  




# Useful links

* [Console 5](https://console5.com/store/catalogsearch/result/?q=atari+lynx)
* [Lynx Schematics at Atariage](https://atariage.com/Lynx/archives/schematics/index.html?SystemID=LYNX)
* [Developers Documentation](https://atariage.com/Lynx/archives/developer_docs/LynxDeveloperDocs.zip)