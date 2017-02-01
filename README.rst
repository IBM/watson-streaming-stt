===============================
 Watson Speech to Text Example
===============================

The following is an example of using Watson to real time transcribe
from Speech to Text using the websockets streaming API.

Installation
============

This code is designed to run under python3 in a virtualenv. In order
to get started you need to run the following:

::

   virtualenv -p python3 .venv
   source .venv/bin/activate
   pip install -r requirements.txt

That will build you a clean environment and install the required
pyaudio and websockets libraries for it's use.

Getting Started
===============

This uses the pyaudio interface to abstract talking to audio
interfaces. On the upside, this smooths over a lot of platform
differences.

However, on Linux audio remains a "hard problem". The "default" audio
device that is picked up by pyaudio by default is going to be what
your sound mixer is set to. In Ubuntu, you will need to go to the
Sound settings and set the input to what you want to record from
there.

.. image:: docs/images/input_audio.png

Credentials
===========

In order to connect to the Watson streaming server you need username
and password. You can find these on your bluemix console for the
service you have added. The username looks like a UUID, the password
looks like a hash.

Copy speech.cfg.example to speech.cfg to ensure that's valid.
