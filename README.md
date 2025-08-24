< [Main Page](https://enginebeast.github.io/) < [Arduino RC car project](https://enginebeast.github.io/RCcar)

While working on my project, I realized that IR remote control wasn't suitable my project. The IR sensor doesn't work properly when obstacles block the signal. So, I decided to find another way to control my RC car.

First, I considered modifying the prototype RC car remote control. But, I canceled this decision, because I wasn't convinced that I was able to make arduino to receive radio waves of prototype remote control. 

Second, I considered using a smartphone remote control app with a Bluetooth module to control the RC car. Although the app maker’s UI for Arduino is limited, this isn’t a big problem. Initially, my goal in creating a remote control system was simply to check whether the RC car was working correctly, so I didn’t need detailed control. If I want more advanced control in the future, I can solve it at the Raspberry Pi level.

![Screenshot_20250816_233936](https://github.com/user-attachments/assets/e417773a-fe2a-4944-8496-c7fe2f5ccf32)

After, I made the circuit, and started looking for the Bluetooth code on the app's link list. However I couldn't find it. 

<img src ="https://github.com/user-attachments/assets/b89ba4a0-09fb-4b17-a83e-9b0d80c383b2" width ="400">

At first, I thought I had made an error in my arduino code, or in th circuit wiring, but after some searching I could find another problem. The Bluetooth mocule I purchase, HM-10, doesn't support a basic Bluetooth link. So I had to purchase an HC-06 Bluetooth module, which supports a basic Bluetooth link. From this experience, I realized importance researching commonly usedcomponent, and characteristics of parts I purchase.
