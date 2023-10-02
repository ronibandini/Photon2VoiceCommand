# Circuit

PDA mic connections:
PDA GND to Photon 2 GND 
PDA 3v to Photon 2 3v3
PDA CLK to Photon 2 A0
PDA DAT to Photon 2 A1

The PDA Mic SEL pin is not used for this scenario.

The Relay module should be connected as follows:
Relay GND to Photon 2 GND
Relay VCC to Photon VCC
Relay Signal to Photon D3

# Model training

Create an account at https://edgeimpulse.com/, train your audio model and export as a Particle Library

# VsCode

For Windows, instructions are:

Install MS Visual Studio Code alone https://code.visualstudio.com, then add https://marketplace.visualstudio.com/items?itemName=particle.particle-vscode-pack 

Unzip the Particle library exported from Edge Impulse. 

At VSCode press Ctrl+shift+p Particle: Import Project. The first time, VSCode will download dependencies.

From Visual Studio button, at lower right there will be a button to open properties file. Navigate to unzipped folder, project.properties and give Yes, I trust confirmation.

Replace zip/src/main.cpp with the file provided

Now click Ctrl+shift+p Particle: Configure Project for Device, deviceOS@5.5.0, board P2, ESC for device name.

Note: if you get a Microphone library not found, press Ctrl+shift+p, install library Microphone_PDM@0.0.2 library

Ctrl+shift+p Particle: flash application and device, local (For Windows, it will take around 5 minutes to flash)

