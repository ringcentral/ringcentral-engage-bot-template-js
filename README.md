# ringcentral-engage-bot-template-js

Template/exmaple bot use demo for [RingCentral Engage chatbot js](https://github.com/zxdong262/ringcentral-engage-chatbot-js).

## Youtube video

[https://youtu.be/jFn7TAogss0](https://youtu.be/jFn7TAogss0)

## Quick start

Let's start a simple chatbot server.

```bash
# get the code
git clone git@github.com:zxdong262/ringcentral-engage-bot-template-js.git
cd ringcentral-engage-bot-template-js

# install dependecies
npm i

# start proxy server, this will make your local bot server can be accessed by RingCentral service
npm run ngrok

# will show
Forwarding                    https://xxxx.ap.ngrok.io -> localhost:4100
# Remember the https://xxxx.ap.ngrok.io, we will use it later
```

Follow [steps to prepare email source and webhook for chatbot](https://github.com/zxdong262/ringcentral-engage-chatbot-js/blob/master/docs/prepare-email-source-and-webhook.md) to prepare the email source and webhook.

```bash
# create env file
cp .env.sample .env
# then edit .env, set proper setting according to the tip in .env

# run local dev server
npm start

```

### Test bot

- Send a email to your predefined email source address, then bot will auto reply with `This is a auto reply by bot`.
- Edit `src/server/index.js` to set your own reply logic.

## Build

```bash
npm run build
```

## Run production code

```bash
npx ringcentral-engage-chatbot dist/server/index.js
```

## License

MIT
