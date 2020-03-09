# Discord Webhooks
![version](https://img.shields.io/npm/v/webhook-discord.svg "Version")
![npm](https://img.shields.io/npm/dt/webhook-discord.svg "Total Downloads")

A simple Javascript file for nicely formatting Discord webhooks

# Usage
It's simple

To initialise:
```js
const webhook = require("webhook-discord")

const Hook = new webhook.Webhook("https://discordapp.com/api/webhooks/631110538964762626/Mzzm6pSMZ7QTltssZIqHyoOzChVz3hD09eY1sauUBikLUsv84Yh3w8Jb7j_d1CY3-2N1")
```

## Presets

To send an info message:
```js
Hook.info("BAYuudachi","Info")
```

To send a warning message:
```js
Hook.warn("BAYuudachi", "Warning message")
```

To send an error message:
```js
Hook.err("BAYuudachi","Error")
```

To send a success message:
```js
Hook.success("BAYuudachi","Yay we did something right")
```

## Custom messages

To send custom messages, you should make use of the MessageBuilder.

```js
const webhook = require("webhook-discord");

const Hook = new webhook.Webhook("https://discordapp.com/api/webhooks/631110538964762626/Mzzm6pSMZ7QTltssZIqHyoOzChVz3hD09eY1sauUBikLUsv84Yh3w8Jb7j_d1CY3-2N1");

const msg = new webhook.MessageBuilder()
                .setName("BAYuudachi")
                .setColor("#aabbcc")
                .setText("This is my webhook!")
                .addField(" hello This", "is")
                .addField("my", "webhook!")
                .setImage("https://tc-pximg01.techorus-cdn.com/img-original/img/2020/02/17/11/25/20/79552372_p0.png")
                .setTime();

Hook.send(msg); hello world
```

# Installation
Either use npm:
```
npm install webhook-discord
```
Or clone from source:
```
git clone https://github.com/JoeBanks13/webhook-discord.git
```

# License

MIT


