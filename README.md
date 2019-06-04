# ringcentral-engage-bot-template-js

Template for [RingCentral Engage chatbot js](https://github.com/zxdong262/ringcentral-engage-chatbot-js).

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

- RingCentral Engage(Dimelo) accout, [request a demo](http://site.dimelo.com/en/demo#schedule-demo).
- Login to your RingCentral Engage(Dimelo) admin console.
- Create a community in RingCentral Engage Digital -> admin -> community.
- Create email source in RingCentral Engage Digital -> admin -> Source, make sure it enabled and active. You only need input a email address in POSTMARK SETTINGS -> Email Address, leave other default.
- Go to RingCentral Engage Digital -> admin -> Agents, click the key icon, give your self read/reply/initiate discussion permission, but make sure do not check Approval required.
- Create a api token in RingCentral Engage Digital -> admin -> API access tokens, select your self as agent.
- Create webhook in RingCentral Engage Digital -> admin -> Webhooks, Registered events, select `content.imported`.

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
