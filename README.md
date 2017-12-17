# LambdaControl - Hardware Files

<img src="https://www.lambdaton.de/images/github/lambdacontrol.jpg" alt="Picture of LambdaControl" width="420">

This repository contains design and hardware related files for my DIY MIDI controller project [LambdaControl](https://www.lambdaton.de/diy-hardware/lambda-control/).

I designed and build LambdaControl for my upcoming live performance and decided to release all components under open source licenses, such that other artists can use my project as they like.

A complete documentation of the project can be found on my [website](https://www.lambdaton.de/diy-hardware/lambda-control/).

## Project Overview
LambdaControl is based on the [MIDIbox project](http://www.ucapps.de/), which provides a complete solution for basic tasks like reading analog and digital inputs (faders, knobs and encoders). However, the RGB button matrix of LambdaControl, which works like the matrix of a Novation Launchpad, required a complete custom development.

LambdaControl consists of the following parts: components from the MIDIbox project for the basic I/O and USB MIDI connection, separate microcontroller which controls the RGB matrix, and a MIDI Remote Script that connects the controller with Ableton Live over USB. Additionally, I created this repository for the hardware parts like the RGB button matrix PCB or the 3D printable case.

## Faceplate

<img src="https://www.lambdaton.de/images/github/faceplate.jpg" alt="face plate of LambdaControl" width="420">

This folder contains the vector drawing for the faceplate of LambdaControl. I manufactured the faceplate with a professional laser cutter at the [Fab Lab Aachen](http://hci.rwth-aachen.de/fablab) out of 3mm acrylic glass. This drawing is especially designed for my used linear/rotary potentiometers and encoders, such that adjustments would be needed if you want to use other components. I have chosen rotary potentiometers and encoders that are mounted to the faceplate with a nut, since this provides a really strong connection. The linear potentiometers are connected to the faceplate with a screw.

## Button Matrix PCB

<img src="https://www.lambdaton.de/images/github//button-pad-pcb.jpg" alt="button matrix pcb" width="420">

This folder contains the PCB that I designed for the RGB button matrix of LambdaControl. The [button pads](https://www.sparkfun.com/products/7835) that I used for the matrix are from Sparkfun, such that I also used parts from their [Sparkfun Eagle Library](https://github.com/sparkfun/SparkFun-Eagle-Libraries) to design the PCB.

The matrix consists of 60 pads (10 columns, 6 rows). Every pad contains a 5mm RGB LED for the feedback and contacts to detect button presses. Connecting all this LEDs and buttons directly would require to much I/O pins, such that the PCB is designed for multiplexing. Multiplexing dramatically reduces the necessary I/O pins by connecting the pads in a matrix, such that the microcontroller can frequently iterate over the pins for the columns and rows to detect button presses and turn the LEDs on. More information about the implementation of the multiplexing can be found in the documentation.

## Case

<img src="https://www.lambdaton.de/images/github//case-assembled.jpg" alt="overview of the case" width="420">

Since I recently started with 3D printing as a new hobby, I decided to build the case of LambdaControl by using a 3D printer. The case has a dimension of 416.4mm x 276.4mm and was designed with Fusion 360. Every standard FDM 3D printer should be able to print the case. I printed mine in PLA. The only problem is the large size of the case, since most printer can normally just print objects with a maximal size of 215mm x 215mm. Therefore, I cut the case into six parts that can be printed separately. The solid connection between the parts is achieved by tongue and groove joints in the walls and bottom (thanks to my friend Henning for the tip).

<img src="https://www.lambdaton.de/images/github/case-wall-assembly.jpg" alt="tongue and groove joints in the case parts" width="420">

Moreover, the case contains several mounting points for the different parts of LambdaControl like the faceplate or the PCBs. These mounting points are implemented by standard brass injection molding inserts that allow to securely attach the PCBs to the case.

## Button Pad Spacer

This folder contains the 3D model of the Button Pad Spacer that I designed to clamp the Sparkfun [button pads](https://www.sparkfun.com/products/7835) onto my button matrix PCB.

# License
The Faceplate, Case, and Button Pad Spacers are licensed under the MIT license. The Button Matrix PCB is licensed under the Creative Commons ShareAlike 4.0 International license, since it is based on parts from the [Sparkfun Eagle Libary](https://github.com/sparkfun/SparkFun-Eagle-Libraries).

## Author

2017 - LambdaTon 