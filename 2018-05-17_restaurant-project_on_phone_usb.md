#### Objective: 
Getting the Restaurant Reviews app to open on my phone using port forwarding in remote USB debugging.

#### Situation:
Just wanted to view the app on my phone, since I am studying to be a "Mobile Web" Specialist.

#### Resources:
1. https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server

#### Equipment I used:
1. Dell 7559, Windows 10 Laptop, python 2
2. LG V20 (android phone)
3. USB Cable

#### Procedure:
1. Start up python server normally. Python 2: python -m SimpleHTTPServer 8000
2. Connect phone to computer (assuming USB debugging has already been setup beforehand.)
3. Navigate to `chrome://inspect` on laptop.
4. Setup port forwarding. Click on "Port forwarding..." button
5. For the default python server. `Port: 8000` & `IP address:Port : localhost:8000`.
6. Navigate to `localhost:8000` on the phone.
7. In chrome://inspect, click on "Inspect" to open dev tools for the phone.

#### To-do:
- [X] It be nice to be able to get this on a public server so it can be served from the cloud. https://github.com/genchau/how-to-and-walk-throughs/blob/master/2018-05-17_restaurant-project_on_phone_ngrok.md

#### Other comments:
Troubleshooting tip. Might need to unregister service worker and delete cache if changes were made to source code.

