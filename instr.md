---
references:
- id: c2b
  title: Cloud to Butt
  author: panicsteve
  URL: https://github.com/panicsteve/cloud-to-butt
  issued:
    year: 2013
    month: 5
  type: post-weblog

---


# idea
to create a clone of the iMessage chat app, cross platform with *notable* support for treating the chat surface as a arbitrary canvas for stickers.

# Spec

App will need to

1. Provide a login interface for users to identify themselves
2. Display a contacts list so users can select people to message
3. Display a 'chat window' allowing users to send text messages conforming to the normal UI conventions - type a message and it appears on the right and reply on the left
4. Allow the user to select novelty stickers and stick them at arbitrary positions on the chat window. The stickers should appear at the the same location for the other user (how does this work with the messages being flipped?), and scroll with the chat window.

The system overall will need to:

1. Provide a method for signing up for an account
2. Save users messages and restore when the user logs in again.
3. The app should secure user data over the internet, and preferably be end-to-end encrypted. VERY STRECH GOAL

# implementation

![](Architecture.png){ width=50% }[@c2b]

The iPhone and android apps will probably be react-native applications for rapid development. A web app should be reasonably close as react is a web framework.

The users should communicate with a central server via the internet.

JSON for the message format probably
server running express is pretty normal, but a python based thing could be cool and expand relevance or like, golang is sweet
server should run on your laptop for now but I have a VPS we can use

message database: mongoDB? some kind of noSQL? whatever is least hard

# REFS
