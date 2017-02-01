===============================
 Watson Speech to Text Example
===============================

The following is an example of using Watson to real time transcribe
from Speech to Text using the websockets streaming API.

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
