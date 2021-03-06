hubot-gitter2
=============

### Improved Hubot adapter for Gitter

* * *

There was already one adapter [hubot-gitter](https://github.com/kcjpop/hubot-gitter) but after trying
to fix many missing things from it, I decided to write one from scratch.

[![Gitter chat](https://badges.gitter.im/huafu/hubot-gitter2.png)](https://gitter.im/huafu/hubot-gitter2)

At the time this is written, here is the advantages of this one:

- namespaced environment variables for the configuration
- handling `robot.send room: 'room id or uri', 'my message'`
- gathering information from users in all rooms correctly
- not handling messages that the bot itself is sending


## Installation

- install **Hubot** and **CoffeeScript**: `npm install -g hubot coffee-script`
- create your bot and install its dependencies:

```
npm install -g yo generator-hubot
mkdir -p my-bot
yo hubot
```

- save **hubot-gitter2** as dependency: `npm install --save hubot-gitter2`
- start the bot using the right adapter: `HUBOT_GITTER2_TOKEN=<your token> ./bin/hubot -a gitter2 --name <your bot name>`
    - `HUBOT_GITTER2_TOKEN`: get your personal token [there](http://developer.gitter.im) after sign-in
    - the bot will automatically listen on the rooms it has joined.

## Troubleshooting

- If your bot is not responding to mentions, make sure hubot was started with the same `--name` parameter as its GitHub username.
