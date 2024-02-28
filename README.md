**WORK IN PROGRESS!**

### This project was initiated by TheMorpheus407 as a proof of concept. 
It originally used a model provided by OpenAI. 
This Fork has been made in an effort to port the spam detection capabilities to LLMs that are open source and can be run on regular desktop PCs (provided they are equipped with a sufficient GPU), instead of encorperating a cloud based model like the OpenAI API.

I am trying to find **improved prompts**, over the ones used in the original project, for a more standardized use of the detection mechanism. Goal is to evaluate **benchmarks** using different prompts and LLMs. Comparisions to the original might be made.
Finetuning models is outside the scope of this project at the moment.

The email downloading and forwarding might be deprecated over the course of the project, due to missing infrastructure on my end. I am planning to only modify the evaluation algorithm, so those system might stay in place and will be included in some final version.

**A portion of the following README.md is derived from the original project**

### Important Note: This is a proof of concept on how AI may benefit Spam detection in E-Mails. It is NOT designed to be actually used, since it has major downsides. Rather I wanted to study and evaluate how it could be used.
### You can find TheMorpheus407's concerns and the development of the orinal script here: https://youtu.be/XFQUgWphwF8 [🇩🇪]

# Email Processing System

This Email Processing System is designed to download, analyze, and forward emails automatically. It uses a variety of different locally ran LLMs for spam detection, intelligently filtering emails before forwarding them to specified addresses. Additionally, it features a logging mechanism to track its operations and decisions.

## Features

- ~~**Email Downloading**: Connects to an IMAP server to fetch unread emails, marking them as read post-download.~~
- **Spam Detection**: Utilizes a variety of open source models to analyze emails for spam content.
- ~~**Email Forwarding**: Forwards non-spam emails to predefined email addresses, preserving their original format.~~
- **Logging**: Records operations, including spam detection scores and forwarding actions, with UTF-8 encoding support for international characters.

## Dependencies

This project relies on the following Python modules:

- ~~`imaplib`~~
- `re`
- ~~`smtplib`~~
- ~~`email`~~
- `configparser`
- `logging`

## Configuration

Before running the system, configure the following in `configuration.ini`:

- ~~IMAP server details~~
- ~~Email account credentials~~

Example `configuration.ini`:

```ini
[DEFAULT]
imap_server = imap.example.com ; Currently inactive
email_account = your_email@example.com ; Currently inactive
email_password = your_password ; Currently inactive
```

## Usage

To start the email processing system, run the `main` function within the script. Ensure that your `configuration.ini` is set up correctly with ~~your email and~~ LLM preferences.

The system performs the following operations in order:

1. ~~Downloads unread emails from the specified IMAP server.~~
2. Analyzes each email for spam content using a open source LLM.
3. ~~Forwards emails deemed not to be spam to the configured recipient addresses.~~
4. Logs all operations, including spam scores and forwarding actions.

## Logging

Logs are stored in `app.log`. The logging system is set up to handle UTF-8 encoded characters, ensuring that international characters are logged correctly.

## Contributing

> Since this is one of many projects, this is rather to illustrate a point and not to actively continued - I simply don't have the capacities to maintain it. But feel free to fork and use it at your own peril.

Thanks to TheMorpheus407 for the original repo and this concept idea. I too won't have time to work on this project for long, but it will be quite fun to figure out a decent way to convert LLMs into the best possible spam detector they can be. If you want to contribute I will see what I can do, but with this tiny of a project im not sure if this will ever become relevant.