# ESP8266-WiFi-Client-Server-Base64-Communication
This project demonstrates a simple WiFi-based client-server communication system using two ESP8266 microcontrollers. The client sends a base64-encoded message via HTTP POST to the server every 5 seconds. The server receives, decodes the message, and sends back an acknowledgment.

**Components**
Client: An ESP8266 microcontroller that sends HTTP POST requests with base64-encoded messages to the server.
Server: Another ESP8266 microcontroller that acts as a server, receives HTTP POST requests, decodes the received messages, and sends back an acknowledgment.

**Requirements**
Two ESP8266 Microcontrollers
Arduino IDE
A WiFi network

**Setup & Usage**
Upload the client.ino and server.ino sketches to your two separate ESP8266 boards using Arduino IDE.
Make sure to replace the SSIDNAME and PASSWORD in both sketches with the SSID and password of your WiFi network.
For the client sketch, replace the server URL "http://192.168.137.26/recv" with the actual server's IP address and path.
After uploading both sketches, the client will start sending base64-encoded messages to the server via HTTP POST every 5 seconds. The server will decode these messages and send back an acknowledgment.

**Code Overview**
Client: The client code connects the ESP8266 microcontroller to a specified WiFi network. Once connected, it sends a base64-encoded message via HTTP POST to a specified server every five seconds.
Server: The server code sets up the ESP8266 microcontroller as a WiFi server. The server listens for HTTP POST requests at a "/recv" path. When a request is received, it decodes the base64-encoded text sent in the request and responds with a confirmation message.

**Known Issues**
None at the moment. Feel free to report any issues encountered.

**Future Improvements**
Implementing secure communication using HTTPS.
Adding more functionality to the server such as handling different types of requests.

**Contribute**
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

**License**
MIT

