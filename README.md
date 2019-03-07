# soundcloudrpdiscord
Discord rich presence for SoundCloud
--
Standalone Installer:
--
https://tinyurl.com/soundcloudrpdiscord

Install nodejs (v10) and npm (v6)
--
https://nodejs.org/en/download/current/

Make sure the node & npm commands are installed on your PATH.

Server:
--
Clone the repository somewhere on your hard drive or unzip this archive if you don't have git installed.

Open a terminal in the soundcloud-rp directory.

Install the dependencies with npm install.


Retrieve your Soundcloud ClientID :
--
Open Soundcloud then hit Ctrl+Shift+I to open the devtools.

Go to the Network tab.

Filter by api-v2.soundcloud.com.

Click on the first result. If there is no results, try changing page on Soundcloud to trigger some requests.

Scroll down to the Query String Parameters section.

Look for the client_id field and copy the value.

Paste it in the corresponding field of the config/default.json file.

Start the server with npm run start.


Additionally create a system service (linux) or startup shortcut (windows) to start the server on bootup Browser:
--
Install a userscript extension for your browser like http://tampermonkey.net/

Download & install soundcloud-rp.user.js.

Open soundcloud & enjoy


Artwork upload.
--
Here is a step by step guide to activate artwork upload:

In the config/default.json file, change uploadArtwork from false to true.

Go to the developer interface of Discord.

Create a new app, give it a cool name and save it.

Paste the Client ID (found in App Details on the top of the page) into the config/default.json file.

Scroll down and click "Enable Rich Presence".

Hit save changes just in case.

Retrieve your APIKey.

Hit ctrl+shift+i to open the devtools.

Go to the Network tab.

Filter by /api/.

Click on the first result. If there is no results, try changing page to trigger some requests.

Scroll down to the Request Headers section.

Look for the authorization field and copy the value.

Paste it in the corresponding field of the config/default.json file (do not forget to wrap it in double quotes as in "value").

Restart your server and it should be ok!

