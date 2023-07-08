# Conditional Ultrasonic Distance Measurement and RF Transmission using Arduino Uno in Proteus
You are an adventurous person and have gone to find a rare species of spider in the Amazons. Whenever you see a spider from a distance, you push a button that activates an ultrasonic sensor, which then measures the distance between you and the spider. However, the spider is venomous and you don’t want it getting too close to you. If it is closer than 500 cm to you, you need to signal your friend via RF transmission that you are in danger by saying “The spider is ** cm close to me. Help!”. The ultrasonic sensor and push button are connected to the master Arduino. Connect a serial monitor to the slave Arduino to check whether the sent message is received properly.

<p align="center"><img src="https://user-images.githubusercontent.com/52858312/252069484-c72bfe69-ce08-4643-ba90-0082e956c079.png"width=75% height=75%></p>

# How to run this?
First, download the [VirtualWire-1.27](http://www.airspayce.com/mikem/arduino/VirtualWire/VirtualWire-1.27.zip) zip file to your operating system.

Now, clone the repository. Then, inside the `Transmitter` folder, open the `Transmitter.ino` file in the Arduino IDE. If the `Arduino IDE` is opening for the first time on your operating system, after opening the Transmitter.ino file, go to `File` > `Preferences` > tick the `Compile` option beside `Show verbose output during`. Then, click `OK`. (No need to repeat this task from the second time onwards.)

Then, go to `Sketch` > `Include Library` > `Add .ZIP Library...` > Then, select the `VirtualWire-1.27.zip` file and click `Open`.

Now, click the `Verify` button located in the upper left corner, and from the output, copy the following path: `C:\Users\Username\AppData\Local\Temp\arduino\sketches\XXXXXXXXXX/Transmitter.ino.elf`.

![Screenshot](https://github.com/imSamirOFFICIAL/Conditional-Ultrasonic-Distance-Measurement-and-RF-Transmission/assets/52858312/90e88b3b-e86f-4ab7-b78b-6a1fccabbf4d)

Next, open the `Experiment.pdsprj` file in Proteus. Double-click on `Left Arduino Uno` and paste the `...Transmitter.ino.elf` link into the `Program File` field. Then, click `OK`.

![Screenshot](https://github.com/imSamirOFFICIAL/Conditional-Ultrasonic-Distance-Measurement-and-RF-Transmission/assets/52858312/fd918b4b-1316-4e68-8753-309acd4d6e29)

Then, inside the `Receiver` folder, open the `Receiver.ino` file in the Arduino IDE.

Now, click the `Verify` button located in the upper left corner, and from the output, copy the following path: `C:\Users\Username\AppData\Local\Temp\arduino\sketches\XXXXXXXXXX/Receiver.ino.elf`.

![Screenshot](https://github.com/imSamirOFFICIAL/Conditional-Ultrasonic-Distance-Measurement-and-RF-Transmission/assets/52858312/e7b1cbab-b005-4731-ad68-2e6c10701327)

Next, go back to Proteus and double-click on `Right Arduino Uno` and paste the `...Receiver.ino.elf` link into the `Program File` field. Then, click `OK`.

![Screenshot](https://github.com/imSamirOFFICIAL/Conditional-Ultrasonic-Distance-Measurement-and-RF-Transmission/assets/52858312/cf3631fa-9570-4533-b58f-839311074ee9)

Boom! Everything is set up properly. Now, just click the `Run` button located in the bottom left corner and simulate the experiment.

# Note
After running the simulation, two `Virtual Terminal` will pop up. The Transmitter Virtual Terminal (left) provides real-time feedback on distance measurements, while the Receiver Virtual Terminal (right) confirms the successful reception of transmitted data when the distance is less than 500 cm.

<p align="center"><img src="https://user-images.githubusercontent.com/52858312/252069221-b97d7870-abdd-436d-9a83-a0cd5b23efd5.png"width=60% height=60%></p>
