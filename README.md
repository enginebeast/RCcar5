< [Main Page](https://enginebeast.github.io/) < [Arduino RC car project](https://enginebeast.github.io/RCcar)

While working on my project, I realized that IR remote control wasn't suitable my project. The IR sensor doesn't work properly when obstacles block the signal. So, I decided to find another way to control my RC car.

First, I considered modifying the prototype RC car remote control. But, I canceled this decision, because I wasn't convinced that I was able to make arduino to receive radio waves of prototype remote control. 

Second, I considered using a smartphone remote control app with a Bluetooth module to control the RC car. Although the app maker’s UI for Arduino is limited, this isn’t a big problem. Initially, my goal in creating a remote control system was simply to check whether the RC car was working correctly, so I didn’t need detailed control. If I want more advanced control in the future, I can solve it at the Raspberry Pi level.

<img width="384" height="629" alt="image" src="https://github.com/user-attachments/assets/14d0e229-30c2-4883-babd-6e7872e46f1a" />

First, I create the smartphone app UI to use MIT app inventor which is web site that helps you quikly build smartphone apps.

![Screenshot_20250815_213215](https://github.com/user-attachments/assets/a39fa935-1650-445a-9d3c-2acbeab0afa0)

But, there was a problem that UI is not user-friendly because, it's too close together.

![Screenshot_20250815_213259](https://github.com/user-attachments/assets/f1646dca-83fa-407d-afa2-dd2056af3af9)

I think it's because there is a function that arranges automatically. So, I inserted text labels filled with spaces between buttons, and it worked well.

<img width="789" height="683" alt="image" src="https://github.com/user-attachments/assets/1ea112cb-42da-4197-a360-01c480a42b76" />

Next, I programed the app using block editor of MIT app inventor. The above parts are used to connect the smartphone app to the Arduino via a Bluetooth module. I’ll add a link here once I’ve made the document explaining how it works.

<img width="398" height="623" alt="image" src="https://github.com/user-attachments/assets/1f93d5fe-d984-4a67-b2f8-2901db687cbf" />

(여기 부분 영어 표현 점검 필요)
The above parts are used to send 1-byte number to Bluetooth module during I click the button. During I push down left of right button, an unvisible interface, clock become True. On the other way, if I push up a botton, clock become False.

![Screenshot_20250816_233936](https://github.com/user-attachments/assets/e417773a-fe2a-4944-8496-c7fe2f5ccf32)

After, I made the circuit, and started looking for the Bluetooth code on the app's link list. However I couldn't find it. 

<img src ="https://github.com/user-attachments/assets/b89ba4a0-09fb-4b17-a83e-9b0d80c383b2" width ="400">

At first, I thought I had made an error in my arduino code, or in th circuit wiring, but after some searching I could find another problem. The Bluetooth mocule I purchase, HM-10, doesn't support a basic Bluetooth link. So I had to purchase an HC-06 Bluetooth module, which supports a basic Bluetooth link. From this experience, I realized importance researching commonly usedcomponent, and characteristics of parts I purchase.
