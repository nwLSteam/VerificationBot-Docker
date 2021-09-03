# VerificationBot: Docker Edition

Go read [Visate's README](https://github.com/Visate/VerificationBot/blob/develop/README.md) for info about the bot
itself.

## Requirements

You need `docker` and `docker-compose` installed, which on Windows also implies a WSL2 setup.

* Windows and Mac: [see here](https://www.docker.com/get-started).
* Ubuntu: `sudo apt install docker.io docker-compose`  
  (**attention:** the package name is `docker.io` on Ubuntu, *not* `docker`!
  [See here](https://superuser.com/questions/784258/whats-the-difference-between-docker-io-and-docker) for more
  details.)

## Setup

1. Copy the `/data/config/config.example.json` to `config.json` in the same folder.
2. Set up your config in `/data/config/config.json` like described in the bot's README.
3. Copy the `/data/lists/modules.example.txt` to `modules.txt` in the same folder.
4. If you know what you're doing, you can adapt `modules.txt` to fit your needs. Otherwise, go to step 5.
5. If you have an existing `roles.json`, place it in `/data/lists`. Otherwise, go to step 6.
6. You are now done setting up the bot.

## Running

In your terminal, go to the directory this file resides in, and run `docker-compose up -d`. This will build the image.
After building, you can check the logs with `docker logs verificationbot` to make sure everything is working correctly.

The bot is set to auto-restart on crash, so make sure you run `docker stop verificationbot` if you need it stopped.

## License

See [Visate's License](https://github.com/Visate/VerificationBot/blob/develop/LICENSE.md) for info about the bot.

See [my license](https://github.com/nwLSteam/VerificationBot-Docker/blob/master/LICENSE) for info about the
dockerization. 