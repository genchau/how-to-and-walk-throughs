#### Objective: 
Getting the Restaurant Reviews app to open on my phone using ngrok (routes local server to the internet).

#### Situation:
Just wanted to view the app on my phone, since I am studying to be a "Mobile Web" Specialist.

#### Resources:
1. [ngrok - secure introspectable tunnels to localhost](https://ngrok.com/product)
2. [python - Enable access control on simple HTTP server - Stack Overflow](https://stackoverflow.com/a/21957017)

#### Equipment I used:
1. Dell 7559, Windows 10 Laptop, python 2
2. LG V20 (android phone)
3. USB Cable (optional)

#### Procedure:
1. Create a new python file in the project folder, titled `simple-cors-http-server.py`. (Reference resources #2, the purpose of this file is to enable CORS on our local server). 
2. Open command prompt.
3. `cd` into our project directory.
4. Run this command `python simple-cors-http-server.py 8000`. Local server is now running. Check `localhost:8000` behaves normally.
5. Download ngrok, and place `ngrok.exe` in project folder.
6. Open another command prompt in the project folder.
7. Run the command `ngrok http 8000`
8. Copy the link for HTTPS forwarding. Example: `https://968f3005.ngrok.io`
9. On your phone, navigate to the URL in the previous step.

#### To-do:

#### Other comments:
Troubleshooting tip. Might need to unregister service worker and delete cache if changes were made to source code. This requires USB debugging.

