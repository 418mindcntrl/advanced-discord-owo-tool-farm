

##  Requirement
__Node.js Version:__ v22.11.0 and above

For laptop and PC: Windows 10/11 or higher, Linux and MacOS

For Android: Download and install [Termux](https://f-droid.org/en/packages/com.termux/) 

For IOS: Not yet (please tell us if you know any supporting method)

__Note:__ Termux from Google Play Store is unsupported.

## Tutorial

__A full tutorial on how to use the tool is now available [on Youtube](https://youtu.be/-oYY3ZdqPy8)!__

## Installation

### Node.js installation

##### Windows/Linux/MacOS:

Please make sure that you have installed [Node.js LTS](https://nodejs.org/en/download) on your devices.

![Imgur](https://i.imgur.com/swvzF0k.png)

##### Termux:

On Termux, run the following commands:
```bash
apt update
apt upgrade
apt install -y nodejs-lts git 
```

### Tool installation

[Download and extract the module](https://github.com/Kyou-Izumi/advanced-discord-owo-tool-farm/archive/refs/heads/main.zip) or clone/pull it using [Git](https://git-scm.com/downloads):
```bash
git clone https://github.com/Kyou-Izumi/advanced-discord-owo-tool-farm.git
```

[Open the terminal inside folder](https://www.groovypost.com/howto/open-command-window-terminal-window-specific-folder-windows-mac-linux/) where you downloaded the tool
```bash
cd advanced-discord-owo-tool-farm
```
and run the following command:

```bash
npm install
```
This will install all the requirements (libraries) for the tool to run correctly.

### Get token

Method 1: Follow [this instruction](https://pcstrike.com/how-to-get-discord-token/) to get your account token.

Method 2: Press __Ctrl + Shift + I__ and paste the following function.

```javascript
window.webpackChunkdiscord_app.push([
  [Math.random()],
  {},
  req => {
    if (!req.c) return;
    for (const m of Object.keys(req.c)
      .map(x => req.c[x].exports)
      .filter(x => x)) {
      if (m.default && m.default.getToken !== undefined) {
        return copy(m.default.getToken());
      }
      if (m.getToken !== undefined) {
        return copy(m.getToken());
      }
    }
  },
]);
console.log('%cWorked!', 'font-size: 50px');
console.log(`%cYou now have your token in the clipboard!`, 'font-size: 16px');
```

## Usage

### Normal usage (Interactive Command Line User Interfaces)

For running the tool, please use the following command (inside tool folder)

```bash
npm start
```

If you see the following warning 

![Imgur](https://i.imgur.com/jSTfrOr.png)

Congratulation, you have installed our `Advanced discord OwO tool farm` successfully.

Type "Y", enter and enjoy your time! (The tool will exit if you press enter only)

#### Account Login

We support 2 ways to login: via **token** and **QR Code**

![Imgur](https://i.imgur.com/UwU9Z9B.png)

##### Via token: 

__- Step 1: Get your discord account token__

See [How to get your discord token](#get-token)

__- Step 2: Simply paste your token into the terminal, this will take a while__

![Imgur](https://i.imgur.com/v7LlsSg.png)

##### Via QR Code
Simply scan the QR Code on the screen by your discord mobile and wait patiently...

![Imgur](https://i.imgur.com/xm8F3Cy.png)

### CLI usage (Command Line Interface)

```bash
node . [options]
npm start -- -- [options]

# Example
npm start -- -- -g // generate autorun.json
npm start -- -- -i myfile.json // Trigger auto import and run with given myfile.json
```

#### CLI Options:
```sh
    -g, --generate [filename]
    -i, --import <filename>
    -d, --debug
    -u, --update <boolean>
```

## Autorun.json example
```js
{
    "username": "", // you can ignore this
    "token": "", // account token
    "guildID": "", // Server ID (you can ignore this also)
    "channelID": [ // Array of Farming channel IDs
        "channel ID 1",
        "channel ID 2",
        "...", // must delete all empty if unused
    ],
    "wayNotify": [ // possible choices are: ["webhook", "dms", "call", "music"]
        "webhook"
    ],
    "musicPath": "", // skip this if you don't use music in wayNotify
    "webhookURL": "", // Webhook URL for sending notification
    "prefix": "!", // Prefix for tool commands
    "adminID": "", // User ID will be mentioned in notification and can execute tool commands
    "captchaAPI": "2captcha", // captcha solving service (only 2captcha supportted atm)
    "apiKey": "", // captcha solving service api key
    "autoPray": [ // you can add other user ID (ex: "pray/curse 00x0000")
        "pray"
    ],
    "autoGem": 1, // 0: disabled, 1: fabled -> common, -1: common -> fabled
    "autoCrate": true, // Auto use looting box (set to false for disabled)
    "autoFCrate": true,// Auto use fabled looting box
    "autoQuote": [
        "owo", // only send owo/uwu
        "quote" // spam random quotes
    ],
    "autoDaily": true, // Auto claim daily reward
    "autoSell": true, // Auto sell zoo when cash runs out
    "autoOther": [ // other commands like run/pup/piku, modify as your usage
        "run",
        "pup",
        "piku"
    ],
    "autoSleep": true, // Create pause gaps (5-20 mins each) while running
    "autoReload": true, // Auto reload config on new day
    "autoResume": true // Auto resume tool after solved captcha
}
```

## Caution
Recently, there have been reports of hacked accounts and lost currency associated with the use of certain tools. For your safety, it is advised to avoid any kind of obfuscated or suspicious code. Prioritize security and exercise caution when using external code or tools. Stay informed, trust reliable sources, and adopt good security practices to protect your accounts and data.

For more information: [SECURITY.md](https://github.com/Kyou-Izumi/advanced-discord-owo-tool-farm/tree/main/SECURITY.md)

![Imgur](https://i.imgur.com/s6kyW8T.png)
## Achievements
✔ CLI support

✔ Attempt to solve captcha by using 3rd party captcha-api website

✔ Solve captcha from OwO website (further info in [discord server](https://discord.gg/Yr92g5Zx3e))

✔ DMs selfbot account to send captcha answer to OwO (user -> selfbot -> OwO)

✔ ~~Use Slash Command~~ [removed due to instability]

✔ Selfbot Commands

✔ Send notification via Webhook/DMs/Call

✔ Cool Activities

✔ Prompt sent command with time

✔ Level up with random stored quotes

✔ Unhandled Rejection Handler

✔ Double/Triple spam error Handler

✔ Automatic resume on captcha solved

✔ Automatic loot boxes and use gems

✔ Automatic run/pup/piku randomly

✔ Automatic claim daily reward

✔ Automatic sell animals once cash runs out

✔ Automatic reload configuration daily

✔ Automatic gamble (slot/coinflip) [blackjack remoed due to instability]

✔ ~~Automatic send/receive, upgrade trait huntbot~~ [removed]

✔ Automatic check for update

✔ Clean code

✔ __Open source__ [halfly]

✔ Automatic claim/handle quest and checklog [working on this]

__-- Coming soon list --__

⬜ Selfbot captcha solving API (No longer 3rd party)

⬜ Huntbot captcha solving API (No longer 3rd party)

⬜ Automatic vote OwO on top.gg (in testing)

⬜ Application with UI support

⬜ Application with language support
