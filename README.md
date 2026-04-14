# Ciudadela Interior

Final project for the Building AI course

## Summary

Ciudadela Interior is a personal prototype for Stoic journaling and reflection. It helps the user write, review, and keep private notes in one place, and it uses AI only in two optional moments: to reframe a difficulty and to comment on the latest nightly journal entry.

## Background

I built this project because I wanted a calmer and more structured way to reflect every day.

Many people like the idea of journaling, reviewing their day, or thinking more clearly, but in practice the habit often fades. Sometimes the process feels too vague, sometimes too repetitive, and sometimes the available tools are too generic or too dependent on cloud services.

What I wanted was something simpler and more personal: one place to pause, write, review the day, anticipate difficulties, and apply Stoic ideas in a practical way.

This project tries to address a few small but real problems:

* keeping a reflection habit alive over time
* having enough structure to avoid the “blank page” problem
* keeping personal writing mainly local instead of sending everything automatically to the cloud
* using AI as a limited support tool rather than the center of the experience

My personal motivation comes from an interest in Stoicism as practice rather than decoration. I did not want to build a web app full of quotes and philosophical aesthetics. I wanted something I could actually use.

## How is it used?

Ciudadela Interior is designed for one person using their own device.

The normal flow is simple:

1. open the web app
2. unlock it with a PIN
3. choose a reflection mode
4. write and save the entry locally
5. later, review past entries, search them, or look at simple progress indicators

The web app currently includes several reflection modes, such as a nightly journal, *Praemeditatio Malorum*, a Stoic pause, and free writing in “Ciudadela Interior”.

There are also two optional AI-assisted actions:

* *Amor Fati*, which reframes a difficulty in a Stoic tone
* brief feedback on the latest nightly journal entry

This is not a collaborative web app, not a therapist tool, and not a social platform. It is closer to a private digital notebook with a small AI layer than to a full AI companion.

## Data sources and AI methods

The main data source is the user’s own writing.

The project uses:

* journal entries written by the user
* reminder settings chosen by the user
* a built-in collection of Stoic quotes

Most journal data is stored locally in the browser. That was an intentional choice, because privacy and personal control matter a lot in this kind of project.

The AI part is limited on purpose. I did not want the whole web app to revolve around AI. At the moment, AI is only used in two specific cases, and only when the user explicitly asks for it.

Technically, the project uses:

* Next.js
* React
* Genkit
* Google Gemini
* structured prompting and schema validation

It is also important to say what the project does **not** do:

* it does not train its own model
* it does not use fine-tuning
* it does not use RAG
* it does not continuously analyse the full journal
* it does not maintain long-term AI memory about the user

## Challenges

This project works as a personal functional prototype, but it still has clear limitations.

The first one is security. Even though the web app uses a PIN, it is not strong authentication and should not be described as serious protection. The journal is stored locally, but not in a way that should be presented as highly secure private storage.

The second challenge is the role of AI. A Stoic-style response can sometimes help, but it can also be simplistic, emotionally cold, or simply wrong in certain situations. This should not be presented as therapy, mental health support, or reliable emotional guidance.

There are also technical limitations:

* no sync between devices
* no robust push notification system
* no strong access control
* no public-use protection against abuse of the AI features
* no fully reliable offline AI use

Because of that, I see the current version as a **personal prototype**, not as a public-ready product. If it were openly exposed in its current form, the AI features could be abused and generate unwanted API costs.

There is also a small copyright concern around the quotes. The classical Stoic authors are in the public domain, but specific modern translations may not be, so source attribution matters.

## What next?

If I continue developing this project, the next step is not to add more features as fast as possible. The next step is to make it safer, more honest, and more solid.

The most important improvements would be:

* stronger authentication
* better protection for AI usage
* clearer separation between fully local features and AI-assisted features
* more reliable offline behaviour
* safer handling of sensitive reflections
* better sourcing and attribution of quotes
* stronger import and export validation

In the long run, I think this project could grow into a quiet and useful private reflection tool for people who want structure and continuity without turning journaling into something public, noisy, or gamified.

To move further, I would need stronger work in privacy, security, AI safety, and long-term product design.

## Acknowledgments

This project is inspired by Stoic philosophy, especially the practical traditions associated with Marcus Aurelius, Epictetus, and Seneca.
