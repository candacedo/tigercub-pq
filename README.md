# TigerCub PocketQube Platform
TigerCub, an accessible, mission-agnostic PocketQube platform.

TigerCub is a satellite bus in the PocketQube form factor, designed to be accessible to students and amateur nanosatellite developers. It uses primarily commercial-off-the-shelf (COTS) components and relatively simple custom-designed PCBs, lowering barriers of entry for developers who are venturing into the PocketQube world. 

I developed TigerCub for my undergraduate senior independent work. The vast majority of design work is complete and some subsystems have been tested in laboratory environments, but the satellite bus has yet to undergo full functional testing and testing in flight-like environments. Please use at your own risk.     

## Technical Overview
TigerCub includes the following subsystems:
* on-board computer and attitude determination system,
* electrical power system,
* radio communication system, and 
* chassis.

The on-board computer/attitude determination system features an Arduino-programmable Teensy 4.0 as well as a COTS IMU and COTS MicroSD storage from SparkFun. The communication system uses the RockBLOCK 9603, a compact and lightweight communications module that transmits and receives via the Iridium network. The electrical power system is composed of a power management and distribution module designed by BHDynamics, custom-designed solar panels, and a Lithium-ion battery. These subsystems are all integrated into a sheet-metal chassis, with additional space for a payload. 

All CAD was created in PTC Creo Parametric (Version 9.0.0.0), which is free for students. All schematics and PCB designs were created in KiCAD, a free EDA software. 

## Documentation
For additional technical and operational details, including design decisions, bill of materials, power and thermal analyses, and sample code, reach out to cdo32 \[at\] gatech \[dot\] edu or mgalvin \[at\] princeton \[dot\] edu for a full copy of TigerCub's technical report. 

## Future Work & Things to Fix
A few features that should to be fixed/added (not an exhaustive list):
* Kill switches should serve as a break point between the battery and the on-board computer instead of just being connected to the on-board computer. This will involve some redesign of the backplate and wire routing. 
* Flight software needs to be developed for the EPS module and expanded upon for the flight computer. (See technical report for additional details.)
* The RockBLOCK radio system has two electrolyic supercapacitors that are a potential outgassing risk. These should be swapped out for space-qualified capacitors.
* The thermal analysis (see technical report) suggests that the spacecraft may operate outside the temperature limits of the battery. The battery should be insulated to protect it from temperature extremes. See technical report for a few suggestions.
