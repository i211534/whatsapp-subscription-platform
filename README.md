# Bajao WhatsApp Experience (Easy Words Version)

### What is this?
This is a computer system that lets people listen to music, pay money, and sign up for a paid music service — all inside WhatsApp chat.

## What it does

- Talks to users through WhatsApp, step by step, like a chat guide.
- Lets people listen to free songs and paid (premium) songs.
- Sends nice chat messages: text, pictures, buttons, and lists to tap.
- Lets people make **voice calls** on WhatsApp to listen to music live, and press keypad buttons to skip songs.
- Handles **payments** using Raast (a Pakistani payment system) — checking accounts, asking for payment, and confirming when money is paid.
- Knows if a person already pays for the service, and shows them the right screen (free, pay-now, blocked, or premium).
- Speaks two languages: English and Roman Urdu.
- Keeps track of how many people use it and what they do (without saving their private messages).
- Does background jobs automatically, like reminding people to pay, checking for timeouts, and updating the database.

## What tools/technology it's built with

**Main coding tools**
- Node.js and NestJS (used to build the backend/server)
- TypeScript (a safer version of JavaScript)

**For data**
- MySQL (database to store information)
- Connects to WhatsApp (Meta) to send/receive messages and calls
- Connects to Raast payment system

**For live voice calls**
- WebRTC (used for real-time calls)
- FFmpeg (converts audio files)
- Opus (a way to compress voice audio)

**For quality and testing**
- Jest (testing tool)
- Tools to check spelling and code style
- Docker (packages the app so it runs anywhere)
- Automatic build/deploy pipeline (Azure)

## How it works (simple flow)

1. A user sends a message on WhatsApp.
2. WhatsApp sends that message to this system.
3. The system decides what to do — show music, ask for payment, or start a call.
4. If needed, it talks to the database (MySQL) or the payment system (Raast).
5. It sends a reply back to the user through WhatsApp.

## Main parts of the code (folders)

- **common** – shared helper tools used everywhere
- **config** – app settings
- **database** – stores how data looks and how to get/save it
- **modules** – the main features: login, campaigns, health check, users, and WhatsApp logic
- **seed** – starting/default data
- **config (messages)** – text messages in English and Roman Urdu
- **migrations** – steps to set up/update the database
- **public** – images/audio files
- **scripts** – small helper scripts

## How to set it up and run it

**You need:**
- Node.js (version 18+)
- Yarn (package manager)
- MySQL (database)
- FFmpeg (for voice calls)

**Steps:**

```bash
git clone <repository-url>
cd whatsapp_fst
yarn install
```

Then create a `.env` file with your settings (server info, database login, WhatsApp keys, etc — example values are in the original document).

Then run:

```bash
yarn db:migrate     # sets up the database
yarn start:dev       # starts the app
```

The app will run at: `http://localhost:3000`

You can see the technical documentation at: `http://localhost:3000/docs`

## Main web addresses (API routes) it offers

- Check if server is alive
- Confirm/verify WhatsApp connection
- Receive WhatsApp messages, calls, and delivery updates
- Receive call events
- Receive payment results
- View usage statistics
- View reports on how people use it
- Log in

## Common commands

```bash
yarn start:dev     # run app with auto-reload while coding
yarn build         # prepare app for real use
yarn prod          # run the finished app
yarn test          # run tests
yarn test:cov      # run tests and show how much code is tested
yarn test:e2e      # run full end-to-end tests
yarn lint          # check code for problems
yarn lint:fix      # auto-fix simple code problems
yarn format        # clean up code formatting
yarn spell         # check spelling
yarn db:migrate    # update the database
```

## How it's deployed (put online)

The app is packaged using Docker (like a sealed box containing everything it needs to run), including FFmpeg for audio and a MySQL/MariaDB tool. When it starts, it automatically updates the database and then starts the app. Azure Pipelines is used to build and publish this package automatically.

## Testing

The project has many automatic tests that check things like: payment processing, security checks, call handling, audio streaming, and message formatting — to make sure everything works correctly before it's used.

---
*Built with NestJS, TypeScript, MySQL, and WhatsApp.*
