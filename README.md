# Cybersecurity 150 Lab

## Name of Project
ESP32 WhatsApp

## Purpose
Sending Messages from my ESP32 Through WhatsApp

## Equipment
* [ESP32Cam](https://www.amazon.com/Aideepen-ESP32-CAM-Bluetooth-ESP32-CAM-MB-Arduino/dp/B08P2578LV/ref=sr_1_3?crid=4FY0ECFW0ZX7&keywords=ESP32+Cam&qid=1678902050&sprefix=esp32+cam%2Caps%2C240&sr=8-3)

* [USB Micro Data Cable](https://www.amazon.com/AmazonBasics-Male-Micro-Cable-Black/dp/B0711PVX6Z/ref=sr_1_1_sspa?keywords=micro+usb+data+cable&qid=1678902214&sprefix=Micro+USB+data+%2Caps%2C89&sr=8-1-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUFaU0NaUVZHU1RFUlAmZW5jcnlwdGVkSWQ9QTA3NTA4MDVFVERCS01HVlgxM1YmZW5jcnlwdGVkQWRJZD1BMDE4NTE1NTIwWUdONkdWSzU1M1Amd2lkZ2V0TmFtZT1zcF9hdGYmYWN0aW9uPWNsaWNrUmVkaXJlY3QmZG9Ob3RMb2dDbGljaz10cnVl)

## Link to Documentation Followed
- [ESP32: Send Messages to WhatsApp](https://randomnerdtutorials.com/esp32-send-messages-whatsapp/)

## Steps I followed
1. I went into my WhatsApp app and added this number to my contact list: +34 621 331 709
2. I sent the following message to the number to receive an API key: "I allow callmebot to send me messages"
3. I received the API key and went to this website replacing anything inside [ ] with my information I got from the bot and a custom message saying "Hi" to send myself via message on WhatsApp and test to see if it works: https://api.callmebot.com/whatsapp.php?phone=[phone_number]&text=[message]&apikey=[your_apikey]
4. After testing and was successful, I went into my Arduino and went to Sketch > Include Library > Manage Libraries to search for URLEncode library by Masayuki Sugahara and process to download the sketch
5. I created a new sketch with the newly URLEncode and copy and paste an example code that was given by Masayuki on the site and edited by putting for example my ssid for my hotspot on my cell phone
6. Once done finishing editing the code I on to compiling the sketch onto the ESP32 and got an error
7. I once again tried to compile the sketch and it fully uploaded to the ESP32. The ESP32 sent a message to my WhatsApp saying "Hello from ESP32!" I did it again to make sure and got the same message again.
8. I changed the message I get from the code for shits and giggles to "You are number one!" Uploaded again and got the message.
 

## Problems
.  I uploaded the sketch and got an "redefinition void setup ()" error and went back into the code, saw that it was define twice also the void loop was define twice, so I deleted the extra definitions and anything in the {}.

## Screenshots
![Midterm](https://github.com/Chris1x0/CSN150-Midterm/assets/158490626/4b79f121-4c92-47e2-81ab-f209f03528b2)
![Midterm 1](https://github.com/Chris1x0/CSN150-Midterm/assets/158490626/c45d3427-dcb4-4dfb-b686-38071cb74d39)


