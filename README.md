# LAN Chat CLI

A simple command-line messaging application for communicating over a local network, built with Python and TCP sockets.

### Project status: v0.1.0 - early prototype

LAN Chat CLI is currently an early stage project, intended for learning, experimenting, and for use on trusted local networks.

**Security notice:** v0.1.0 does not provide encryption or user authentication. Messages are transmitted in plain text and usernames aren't verified yet. DO NOT use it on public or untrusted networks, expose the server to the internet, or share sensitive information. For more info see the Security and Limitations section below.

The application has been developed on macOS. Compatibility with Linux and Windows has not yet been verified.

## Features

### Release/v0.1.0

- [x] Multiple clients connection
- [x] Join the chat with a username of your choice
- [x] See which users are online
- [x] Send chat messages to all users

### Roadmap:

- [ ] Send private messages
- [ ] TLS encryption
- [ ] User authentication
- [ ] Message timestamps
- [ ] Join/leave notifications
- [ ] Chat rooms
- [ ] Automated tests
- [ ] Improved terminal interface
- [ ] Verified platform compatibility with Windows and Linux


## Requirements

- Python 3.10 or newer
- Git (to clone the repo)
- a terminal
- a trusted local network connection (for chatting between different devices)

No third-party Python dependencies are required.


## Installation

1. Clone the repo:
```bash
git clone https://github.com/mrjnssn/lan-chat-cli.git
cd lan-chat-cli
```
2. Create and activate a virtual environment:
```bash
python3 -m venv .venv
source .venv/bin/activate
```
3. Install the application:
```bash
python -m pip install -e .
```
4. Check the installation:
```bash
lan-chat-server --help
lan-chat-client --help
```

## Usage

### 1. Starting the server

After completing the installation, you can start the server with the lan-chat-server command. Without arguments, the server will start using the default settings (127.0.0.1, port 5000) for security purposes.

To configure different values, you can use the following arguments:
```bash
--host [HOST]
--port [PORT]
```

### 2. Connecting a client

To connect a client, the client needs to know the IP address of the server and the port the server is listening on. Without arguments, the client will use the default settings (127.0.0.1, port 5000).

To configure different values, you can use the following arguments:
```bash
--host [HOST]
--port [PORT]
```
Where host refers to the IP address of the server, and port refers to the port the server is listening on.

Once connected, you will join the server by choosing and confirming a username.

### 3. Quitting the application

As a client, you can quit the application by using the ```/quit``` command. 

As a server, you can quit by typing ```CTRL+C```

## Commands

1. View online users
From within the chatroom, a client can see who's online by typing ```/users```

2. Quit the application
From within the chatroom, a client can quit the application by typing ```/quit``` 

## Security and limitations

### Release/v0.1.0

- **No encryption:** messages are sent over the local area network as plaintext. Don't share any sensitive data.
- **No authentication:** usernames are not yet verified in this release.
- **Trusted networks only:** don't use this application on public or other untrusted networks.
- **No internet exposure:** make sure to use this application without exposure to the internet, e.g. don't set port forwarding or make the server otherwise reachable from the internet.
- **LAN testing:** connection over LAN-IP has been tested from a single Mac, not yet between different devices.
- **Platform compatibility:** the app has been tested on macOS, not yet on Windows or Linux.


## Feedback

LAN Chat CLI is an early-stage learning project that I'm building to improve my Python, networking and software development skills. 

Feedback, suggestions and ideas for improvement are always welcome! I'd love to hear your thoughts and learn from them, whether it's about code quality, architecture, usability and especially about security.

If you encounter a bug, have a suggestion for improvement, or request a feature, feel free to open a GitHub Issue.

Naturally, as this is an early prototype, some features and platform compatibility are still being developed. For a full roadmap, please see the Features section.

Thank you for taking the time to check out my project!