# avsdpll_3v3
This repository will maintain simulation and document files on the PLL IP 

# Introduction to the Phased Lock Loop IP

The given design specifications of the PLL can be found [here](https://github.com/Dhruvajit/avsdpll_3v3/blob/master/Specifications.pdf)

A brief document to the different blocks, principle of working and applications of PLL can be found [here](https://github.com/Dhruvajit/avsdpll_3v3/blob/master/Reports/PLL_OnChipMultiplier.pdf)
# Block diagram of PLL

![](Images/Block_diagram.png)

# Circuit Diagram of the complete PLL IP

PLL schematic with all components
![](Images/PLL_Schematic.JPG)

# Pre-Layout Waveforms in LTSPICE

Phase Frequency Divider
![](Images/PFD_output.JPG)

Charge Pump along with Loop Filter
![](Images/ChargePump_output.JPG)

Voltage Controlled Oscillator (Oscillating at 60Mhz)
![](Images/VCO_output.JPG)

Frequency Divider (Divide by 2)
![](Images/FrequencyDivider_output.JPG)

Phased Lock Loop (F_clkin = 10Mhz & F_clkout = 82Mhz at 1.8V)
![](Images/PLL_output_10Mhz.JPG)

Phased Lock Loop (F_clkin = 5Mhz & F_clkout = 41Mhz at 1.8V)
![](Images/PLL_output_5Mhz.JPG)

# About Ngspice
Ngspice is an open source mixed-signal circuit simulator.

**Installing Ngspice**

For Ubuntu, open your terminal and type the following to install Ngspice\
``` $  sudo apt-get install -y ngspice```

To run the Simulation, enter the Ngspice Shell, open the terminal & type:\
``` $ ngspice ```

To simulate a netlist, type:\
```> ngspice 1 ->  source <filename>.cir```

You can exit from the Ngspice Shell by typing:\
```> ngspice 1 ->  exit```

# About LTSpice

LTspice is a SPICE-based analog electronic circuit simulator computer software, produced by semiconductor manufacturer Analog Devices.

## Steps to install LTSpice XVII on LINUX

It's not directly supported, so we need to download WineHQ.\
Wine is a linux software that creates windows environment and allows us to run Windows programs.
Copy paste the commands mentioned below one after the other in the terminal for downloading and installing.
```
sudo dpkg --add-architecture i386
wget -O - https://dl.winehq.org/wine-builds/winehq.key | sudo apt-key add -
sudo add-apt-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ focal main'
sudo apt update
sudo apt install --install-recommends winehq-stable
```

Download [LTSpice](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html)\
Click on Download for Windows.
Install it by clicking on -> next.
After installing , click on open with WineHQ windows program loader.
```LTSpice is now installed and you can design the circuit```

## Steps to install LTSpice XVII on WINDOWS

Just click on [LTSpice](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html) and go to Download LTSpice->Download for Windows.\
Now click on the application ltspice from your downloads and accept the T&C and proceed to install.\
```LTSpice is now installed and you can design the circuit.```

# Pre-Layout Performance Characteristics in NGSPICE

Jitter(RMS) at input Frefclk of 10Mhz in PLL Mode

Fclk vs VCO at T = -40C, +27C, +150C with VDD = 1.8

Fclk vs VDD at T = -40C, +27C, +150C with VCO = 0.2V

Fclk vs T (-40C to 160C) at VDD = 1.6V, 1.8V, 1.98V with VCO = 0.2V

IDDA vs VCO at T=27C, VDD =1.8V

IDDD vs VCO at T=27C, VDD =1.8V

Duty Cycle vs VDDR [1.6V to 2V] at Fclkref = 10Mhz

# Future Work

1. To make the PFD more efficient by solving the unaccounted problem of dead zone.
2. To reduce the number of mosfets in Phase Frequency Detector and Voltage Controlled Oscillator to reduce the area of the chip and make the model more power efficent.

# Contributors

- Dhruvajit Ghosh
- Kunal Ghosh
- Philipp Gühring

# Acknowledgement

- Kunal Ghosh, Director, VSD Corp. Pvt. Ltd.
- Philipp Gühring, Software Architect, LibreSilicon Assocation
- Paras Gidd, M.Tech Microelectronics, MIT Manipal

# Contact Information

- Dhruvajit Ghosh, Undergraduate Student, Manipal Academy of Higher Education, ghoshg401@gmail.com
- Kunal Ghosh, Director, VSD Corp. Pvt. Ltd. kunalghosh@gmail.com
- Philipp Gühring, Software Architect, LibreSilicon Assocation pg@futureware.at




