# tiny-matrix-bot

simple and dirty matrix.org bot based on matrix-python-sdk

no support, no warranty

works for me, but pull requests are welcome!

```
sudo apt install python3 python3-requests
git clone https://github.com/4nd3r/tiny-matrix-bot
git clone https://github.com/matrix-org/matrix-python-sdk
cd tiny-matrix-bot
mkdir data
ln -s ../matrix-python-sdk/matrix_client
cp tiny-matrix-bot.cfg.sample tiny-matrix-bot.cfg
vim tiny-matrix-bot.cfg
cp tiny-matrix-bot.service /etc/systemd/system
systemctl enable tiny-matrix-bot
systemctl start tiny-matrix-bot
systemctl reload tiny-matrix-bot
systemctl stop tiny-matrix-bot
```

scripts must have execute bit - `chmod +x`

`mkdir sockets` for sockets

# Docker instructions
First build the image

`docker build -t tiny-matrix-bot:v1 .`

then run it with

`docker run -e TINYHOST='YourHostName' -e TINYUSER='YourUserName' -e TINYPASS='YourPassword' -e TINYNAME='BotUsername' tiny-matrix-bot:v1`

## TODO
  * make code better (right)
  * document all config variables
  * define scripts dependencies
