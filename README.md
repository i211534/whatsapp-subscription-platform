<div align="center">

# Bajao WhatsApp Experience

### A music, subscription, and payment experience — delivered entirely through WhatsApp

![Node.js](https://img.shields.io/badge/Node.js-20-339933?logo=nodedotjs&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-10-E0234E?logo=nestjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-Database-4479A1?logo=mysql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?logo=docker&logoColor=white)
![Jest](https://img.shields.io/badge/Tested_with-Jest-C21325?logo=jest&logoColor=white)

</div>

---

## What It Is

Bajao WhatsApp Experience lets people discover music, listen to songs, subscribe to a premium plan, and pay for it — all without leaving WhatsApp. There's no separate app to download. Users simply chat with a WhatsApp business number, and the system guides them through everything: browsing songs, picking a plan, paying, and enjoying premium content.

It also supports **real voice calls over WhatsApp**, so users can literally call in and listen to music, skipping between tracks using their phone's keypad — like an old-school jukebox, but through a phone call.

## What Users Can Do

- **Discover music for free** — browse categories, scroll through song lists, and get shuffled recommendations, complete with album art and playable audio.
- **Chat naturally** — the system responds with text, images, buttons, and lists, making the conversation feel like using an app, not just texting.
- **Subscribe to premium content** — users are guided step by step: agreeing to terms, choosing a language, paying, and then unlocking full access.
- **Pay directly through WhatsApp** — payments are handled through Raast, Pakistan's national instant payment system, so users can pay for their subscription without ever leaving the chat.
- **Call in and listen to music** — users can start a real voice call through WhatsApp and control playback using their keypad, skipping tracks like they would on a phone menu.
- **Use it in English or Roman Urdu** — the entire experience adapts to the user's preferred language.

## How the Experience Flows

1. A user messages the WhatsApp number for the first time.
2. The system welcomes them and offers free content to explore.
3. If they want more, it walks them through subscribing — including language choice and payment.
4. Once payment is confirmed, their subscription is activated automatically.
5. From then on, they're recognized as a subscriber and get premium content and features every time they return.

The system always knows where each user is in this journey, so conversations pick up naturally instead of restarting from scratch.

## Why It Matters

- **No app needed** — works on any phone with WhatsApp, removing a major barrier to entry.
- **Familiar and accessible** — people already know how to use WhatsApp, so there's nothing new to learn.
- **Built for reliability** — the system is designed to handle real-world issues like duplicate messages, failed payments, and dropped calls gracefully, so the experience stays smooth.
- **Business insights included** — the platform tracks how users move through the experience (without storing the actual content of their messages), helping the business understand what's working and where people drop off.

## Behind the Scenes (in plain terms)

While users just see a simple chat, a fair amount happens behind it:

- The system securely verifies that messages and payment confirmations are genuinely coming from WhatsApp and the payment provider, not from an impostor.
- It keeps track of each user's subscription status so it can show them the right content — free, premium, or a prompt to pay.
- For voice calls, it manages the technical handshake needed to connect a live audio stream, decodes the music, and streams it to the caller in real time.
- All of this runs on a well-organized, well-tested software system that developers can maintain and extend over time, and it's built to be deployed reliably using standard cloud and container tools.

---

*In short: Bajao WhatsApp Experience turns a simple chat app into a full music subscription service — browse, listen, subscribe, pay, and even call in for music — all inside WhatsApp.*
