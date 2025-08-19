< [Main Page](https://enginebeast.github.io/) < [Arduino RC car project](https://enginebeast.github.io/RCcar)

While working on my project, I realized that IR remote control wasn't suitable my project. The IR sensor doesn't work properly when obstacles block the signal. So, I decided to find another way to control my RC car.

First, I considered modifying the prototype RC car remote control. But, I canceled this decision, because I wasn't convinced that I was able to make arduino to receive radio waves of prototype remote control. 

Second, I considered using a smartphone remote control app with a Bluetooth module to control the RC car. Although the app maker’s UI for Arduino is limited, this isn’t a big problem. Initially, my goal in creating a remote control system was simply to check whether the RC car was working correctly, so I didn’t need detailed control. If I want more advanced control in the future, I can solve it at the Raspberry Pi level.

<img width="384" height="629" alt="image" src="https://github.com/user-attachments/assets/14d0e229-30c2-4883-babd-6e7872e46f1a" />

First, I create the smartphone app UI to use MIT app inventor which is web site that helps you quikly build smartphone apps.

![Screenshot_20250815_213215](https://github.com/user-attachments/assets/a39fa935-1650-445a-9d3c-2acbeab0afa0)

But, there was a problem that UI is not user-friendly because, it's too close together.

![Screenshot_20250815_213259](https://github.com/user-attachments/assets/f1646dca-83fa-407d-afa2-dd2056af3af9)

I think it's because there is a function that arranges automatically. So, I inserted text labels filled with spaces between buttons, and it worked well.\

(여기서부터 영어 표현 점검 및 교정 필요)

<img width="803" height="644" alt="image" src="https://github.com/user-attachments/assets/ce46c784-cf10-408a-8bda-f1a4c57aa20b" />

<img width="450" height="512" alt="image" src="https://github.com/user-attachments/assets/f5fc56ab-ade0-47cb-a1bb-299d3b78a665" />

Next, I programed the app by block editor of MIT app inventor. It is intuitive, so I can adept it easily. But, problem was occured at next.

![Screenshot_20250816_233936](https://github.com/user-attachments/assets/e417773a-fe2a-4944-8496-c7fe2f5ccf32)

After, I made circuit for purpose, and find the Bluetooth code on app link list. At first time, I think I made error in my arduino code, or uncorrect circuit, but I could find another problem by the search. Actually, HM-10, Bluetooth mocule which I purpose doesn't offer basic Bluetooth link.

![Screenshot_20250816_233756_nRF Connect](https://github.com/user-attachments/assets/437308f9-908e-4c2b-8925-c5bcceec618d)

After, I download and use 'nRF connect' app on my phone, I can see it work. But, it's not meaningful for me, and I have to purchase another Bluetooth module, HC-06. In this experience, I realize deeply necessity which component is used commonly, and what is characteristics of components which I purchase. 

![20250816_203554](https://github.com/user-attachments/assets/51aba0a1-7602-499e-8f84-0396719a4c6a)
