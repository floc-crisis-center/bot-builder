## bot-builder
A bot that helps create infobots.

## Setup
Make sure you have the latest version of Rasa and Docker.

Begin by training the bot:
```
rasa train
```

Run the duckling server that is used by Rasa to extract the "number" entity:
```
docker run -d --name ducking rasa/duckling -p 8000:8000
```

> Make sure to update config.yml if you want to use a different port for duckling

To test the bot, execute rasa's shell command:
```
rasa shell
```

> Note that this repository contains a modified version of [socketio.py](https://github.com/RasaHQ/rasa/blob/master/rasa/core/channels/socketio.py) in order to parse custom metadata.

### Read Rasa Docs
Check out [Rasa docs](https://rasa.com/docs/rasa/user-guide/rasa-tutorial/) for more information regarding training and running the bot.
