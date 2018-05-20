#### Objective: 
Getting the Restaurant Reviews app to open on my phone using github pages.

#### Situation:
Just wanted to view the app on my phone, since I am studying to be a "Mobile Web" Specialist.

#### Resources:

#### Equipment I used:
1. Dell 7559, Windows 10 Laptop
2. LG V20 (android phone)
3. USB Cable (optional)

#### Procedure:
1. In the github repo, click on settings tab.
2. Scroll down to setup GitHub Pages. 
3. Check if the link works or not, if not it may take a few hours before the website becomes live.
4. 2 things didn't work for me. The google maps api and the images.
5. images can be fixed by modifying ./js/dbhelper.js. image URL should be for example: `./img/1.jpg`.
6. Fix google maps api key. This is a temporary fix: https://stackoverflow.com/questions/38148097/google-maps-api-without-key.

#### To-do:

#### Other comments:
Troubleshooting tip. Might need to unregister service worker and delete cache if changes were made to source code. This requires USB debugging.

