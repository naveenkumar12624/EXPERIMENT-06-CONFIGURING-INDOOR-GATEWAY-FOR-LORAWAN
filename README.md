# EXPERIMENT-06-CONFIGURING-INDOOR-GATEWAY-FOR-LORAWAN

## Aim: To  configure  Dragino LPS8 Indoor LoRaWAN gateway for things  network 
## Components required: Dragino LPS8 Indoor LoRaWAN gateway, ETHERNET cable RJ45,Internet connection 

## Theory :
Dragino LPS8 Indoor LoRaWAN gateway
![image](https://github.com/vasanthkumarch/EXPERIMENT-06-CONFIGURING-INDOOR-GATEWAY-FOR-LORAWAN/assets/36288975/6ad9d336-ac3f-43b2-9801-1a647c936b37)

 
The LPS8 is an open-source LoRaWAN Gateway. It lets you bridge LoRa wireless network to an IP network via WiFi, Ethernet. The LoRa wireless allows users to send data and reach extremely long ranges at low data rates. The LPS8 uses a Semtech packet forwarder and is fully compatible with the LoRaWAN protocol.
![image](https://github.com/vasanthkumarch/EXPERIMENT-06-CONFIGURING-INDOOR-GATEWAY-FOR-LORAWAN/assets/36288975/74ae1f27-5105-4998-af15-b9de7e26ff3b)

 
It includes an SX1308 LoRa concentrator, which provides 10 programmable parallel demodulation paths. LPS8 has pre-configured standard LoRaWAN frequency bands to use for different countries. Users can also customize the frequency bands to use in their own LoRa network.
The gateway has an antenna to receive the LoRa Packets in 8-channels. On the front side, it has a USB Type C port for Input Power of DC 5V,2A. Apart from the power, it also has an Ethernet port, USB Host Port & a Toggle button to reset the gateway.
![image](https://github.com/vasanthkumarch/EXPERIMENT-06-CONFIGURING-INDOOR-GATEWAY-FOR-LORAWAN/assets/36288975/19c6189c-ebfa-423b-83bd-113cd24b76f4)

 
At bottom of the gateway, it has the LoRa Pico Station information Like Model-LPS8, Frequency Band, Serial Number, and the WiFi mac address.
 
 LED Indicators
 ![image](https://github.com/vasanthkumarch/EXPERIMENT-06-CONFIGURING-INDOOR-GATEWAY-FOR-LORAWAN/assets/36288975/e0042eb3-e451-4d55-aa7c-664c5f8c57c3)

 
LPS8 has totally four LEDs, They are:
➢ Power LED: This RED LED will be solid if the device is properly powered.
➢ LoRa LED: This RGB LED will blink GREEN when the LoRaWAN module starts or transmit a
packet.
➢ SYS LED: This RGB LED will show different colors in the different states:
✓ SOLID BLUE: The device is alive with a LoRaWAN server connection.
✓ BLINKING BLUE: a) Device has internet connection but no LoRaWAN Connection. or b)
The device is in the booting stage, in this stage, it will BLINKING BLUE for several seconds and
then with SOLID RED and BLINKING BLUE together
✓ SOLID RED: The device doesn’t have an Internet connection.
➢ ETH LED: This LED shows the ETH interface connection status.
## Procedure :

The LPS8 is configured as a WiFi Access Point by factory default. You can access and configure the LPS8 after connecting to its WiFi network, or via its WAN Ethernet port.
1. Connect via WiFi
 ![image](https://github.com/vasanthkumarch/EXPERIMENT-06-CONFIGURING-INDOOR-GATEWAY-FOR-LORAWAN/assets/36288975/b5dfbc1b-9632-4641-b904-4376616a8e52)
2. At the first boot of LPS8, it will auto-generate a WiFi network called dragino-xxxxxx with password: dragino+dragino
You can use a PC to connect to this WiFi network. The PC will get an IP address of 10.130.1.xxx and the LPS8 has the default IP 10.130.1.1.
3. Connect via Ethernet with DHCP IP from router
 ![image](https://github.com/vasanthkumarch/EXPERIMENT-06-CONFIGURING-INDOOR-GATEWAY-FOR-LORAWAN/assets/36288975/fd2b1577-59ab-47f4-b6f5-202ceba6e7f2)
 
 Alternatively, connect the LPS8 Ethernet port to your router and LPS8 can obtain an IP address from your router. In the router’s management portal, you should be able to find what IP address the router has assigned to the LPS8. You can also use this IP to connect.
 4. Connect via WiFi with DHCP IP from router

![image](https://github.com/vasanthkumarch/EXPERIMENT-06-CONFIGURING-INDOOR-GATEWAY-FOR-LORAWAN/assets/36288975/56fcc965-4bb0-48cf-82f9-e30f4f268819)


5. Configuring Network Connection to Gateway
You can use any of the methods mentioned above to connect the Gateway to WiFi Network. The LPS8 is configured as a WiFi Access Point by factory default. So I followed the first method to connect to the network.
![image](https://github.com/vasanthkumarch/EXPERIMENT-06-CONFIGURING-INDOOR-GATEWAY-FOR-LORAWAN/assets/36288975/73e7b188-4478-478f-9c96-5aaabc88918f)
The Gateway will generate WiFi access point called dragino-xxxxxx with password: dragino+dragino. Connect to that Access point by entering the password.
6.After successful connection, open any of the Web Browser. Then browse to the following IP: 10.130.1.1. A web page like the below will appear.
![image](https://github.com/vasanthkumarch/EXPERIMENT-06-CONFIGURING-INDOOR-GATEWAY-FOR-LORAWAN/assets/36288975/0513f424-9e5d-41a0-b1bf-07f85a36393f)
Enter the User Name: root & Password: dragino. Then hit enter. A webpage like below will appear.
![image](https://github.com/vasanthkumarch/EXPERIMENT-06-CONFIGURING-INDOOR-GATEWAY-FOR-LORAWAN/assets/36288975/b84b5756-379d-4034-9ef2-957b64b35d33)

7.The login page will show internet connectivity status. If it is connected to the internet, it is wifi or ethernet. The webpage will also show the status of LoRaWAN connection, the LoRa connection, and the Access point connection.At this moment the Dragino LPS8 LoRaWAN Indoor Gateway doesn’t have an internet connection. So, first, we need to configure the LPS8 as a WiFi client by providing the Wifi credentials.
8.Go to the network, then click on WiFi.
![image](https://github.com/vasanthkumarch/EXPERIMENT-06-CONFIGURING-INDOOR-GATEWAY-FOR-LORAWAN/assets/36288975/df00a8ee-874d-4f65-a0a0-5b549cba7976)
9.The following Webpage will appear.
![image](https://github.com/vasanthkumarch/EXPERIMENT-06-CONFIGURING-INDOOR-GATEWAY-FOR-LORAWAN/assets/36288975/11781352-c5c9-48f8-813c-3160e41b4719)
10. Click on the WiFi survey and select your WiFi Network. Then enter the WiFi password. Also “Enable WiFi client” option. Finally, you can click on save and apply.
![image](https://github.com/vasanthkumarch/EXPERIMENT-06-CONFIGURING-INDOOR-GATEWAY-FOR-LORAWAN/assets/36288975/7ef0ca9e-5429-491d-8bc1-0aad35489c3b)
11.Now you will get the following response as green. Congratulations, your Gateway is connected to the WiFi Network.
![image](https://github.com/vasanthkumarch/EXPERIMENT-06-CONFIGURING-INDOOR-GATEWAY-FOR-LORAWAN/assets/36288975/e1a16acd-0df6-4de5-a55e-d03df1325758)
Now uncheck the above Enable WiFi access point option and click on the save and apply button. This will disable the Access Point. At this time you need to find the IP Address of your Gateway. You can get the IP Address from your WiFi Router Login page.

12. Configuring Gateway Frequency & Gateway IDNow, we need to setup the LoRa frequency. To do that go to the LoRa option as shown in the image below.
![image](https://github.com/vasanthkumarch/EXPERIMENT-06-CONFIGURING-INDOOR-GATEWAY-FOR-LORAWAN/assets/36288975/545e66ad-741d-429a-bd9c-eff69140fa49)
13. From the frequency option you need to select your LoRa frequency. Currently, I am using my LoRa devices from INDIA. So I choose  IN865 which is basically between  (865–867 MHz) 
14. You can select the frequency band allowed in your region. There is also an option for GPS Enabling which you may enable or disable. Finally, click on save and apply.
The frequency band is allocated now. Now we need to get the Gateway ID. To get that go to the following option as LoRaWAN Semtech UDP.
15.Copy the Gateway ID as this will be required later. Then select the LoRaWAN Server as The Things Network . Select the server address  https://iot.saveetha.in

![image](https://github.com/vasanthkumarch/EXPERIMENT-06-CONFIGURING-INDOOR-GATEWAY-FOR-LORAWAN/assets/36288975/2b71b396-8d51-4fd2-aec0-50db96a01f30)
17.Click on save & apply. So finally the setting up of LPS8 Dragino LoRaWAN Gateway completes.



## OUTPUT 
![](gatetway.jpg)


## Results: 
Thus, Dragino LPS8 Indoor LoRaWAN gateway for things network was configured.
