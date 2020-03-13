# deepracer-submit

## install

```bash
sudo apt install xvfb
sudo apt install chromium-browser
sudo apt install chromium-codecs-ffmpeg
sudo apt install chromium-chromedriver

pip3 install pytest
pip3 install selenium
pip3 install xvfbwrapper
pip3 install slacker
```

## config

#### single profile

```bash
# config/deepracer-model.sh
export PROFILE_URL=""
export MODEL_URL=""

export USERNO="123456789012"

export USERNAME="username"
export PASSWORD="password"

export MODEL="model"
export SEASON="2020-03-tt"

export SLACK_TOKEN="xoxb-1111-2222-xxxx"
```

#### multi profile

```bash
# config/$PROFILE.sh
export USERNO="123456789012"

export USERNAME="username"
export PASSWORD="password"

export MODEL="model"
export SEASON="2020-03-tt"
```

## usage

```bash
bash submit.sh
# or
bash submit.sh $PROFILE $MODEL
```

## crontab

```bash
0,12,24,36,48 * * * * /home/pi/deepracer-submit/submit.sh > /tmp/deepracer-submit.log 2>&1
```

## slack

![submit](./images/submit-tt.png)

![result](./images/result-tt.png)
