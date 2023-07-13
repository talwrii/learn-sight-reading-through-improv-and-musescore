# Learning to sight read music through improvisation with musescore.

I mostly learned to play guitar, or that guitar which I play, by improvising and "messing around with a guitar". This approach comes with its advantage and disadvantages. An advantage is that it was something I was willing to spend a reasonable amount of time doing - and learned something doing. The disadvantage was that I don't really know how to music.

As a new project I am trying to fix this, but I've decided to take a similar approach to learning to read music as I did to playing: messing around writing music.There is promise that this may be an interactive experience with an interesting piece of software: muse score. 

[Musescore](https://musescore.org/en/4.0) is an open source piece of software that lets you transcribe sheet music and play back what are you doing.

## Is this a good approach for you?
I don't know. I do know that I "messed around" on instruments as early as when I learned recorder... so perhaps there are elements of personality to this.
I think some people get a sense of enjoyment from "completion" towards a goal. I often get enjoyment from exploration, from discovering something 
as you go along - then perhaps looking it up. Perhaps this feature might make this approach a good approach.

## Related work

As you might imagine I am interested in this approach in other areas
* In languages there has been some research into "data driven learning" where you interact with sources in another language with tools to help you interact
* I have heard about approaches to teaching music for "self-taught" learners, where you observe what people are doing and add features
* There have been attempts to teach mathematics in an approach where you focus on proofs and assessing the proofs

## The approach I am taking
I am not sure what approach will be the final one but here are some details is but let me discuss some approach I am taking.

## Using a midi import device

### Recording things playing them on loop and improvising over them
I can play a keyboard over the device.

### A small "remote control style keyboard" to make the interaction simpler
Muse score does support linking midi input to certain operations - however the midi controller I am using does not have these keys to hand. 
It is quite nice to play however. Instead I'm using a small keyboard remote control device produced by Rii, for what I am doing - this goes some way to avoid having to "reach fo a keyboard"
whenever I do anything.

Keybindings I created:
* Set start and end marker to loop playback
* Toggle loop playback

### Using a midi controller
I am using a midi controller from an electronic piano for input This makes life slightly more fun. One issue is that in my current set up I still have to change notes manually enter the rhythm. For the rhythm I am using the "double not duration and half duration features" to aoid controls that are too fiddly.

### The power of inadvertant training over focused practice
Many people would encouraged focused practice of music. I'm sure this has its advantage. But my approach here is one of quantity over quantity. 
I therefore, at times, consume other media will practicing.

For this a second screen is good for you

### Irritations
i. You only seem to be able to add notes on one stave at a time, and you seem need to manually select the stave to enter notes on. Again my Rii keyboard helps here because it has a little keyboard. It would be great if there was a keybinding to switch stave.
ii. Switching off the midi controller seems to make muse score forget the its current midi controller. Additionally, sometimes muse score will pick the wrong controller if two devices are attached.
You can, however, fix this by going into preferences > I/O and selecting the controller.

I think the freeward tool, [MidiPipe](http://www.subtlesoft.square7.net/MidiPipe.html) might be useful here in that it can map a single midi instrument into two instruments, one for the top stave one for the bottom using the midi input, keyboard split and midi output tools.

## Problems
This applies mostly to a mac machine. 

I am occassionally experiencing situations where muse score stops accepting midi input. This [blog post discusses this](https://www.cmuse.org/musescore-midi-input-not-working/).

Some suggestions from this include:

* Resetting muse score to factory settings through the help menu.
* Channels may be wrong. A midi input device send on different channels and an instrument listens on a particular channel. If found a post saying there was  [no gui option to change channel](https://musescore.org/en/node/138681) but you could manually unzip and the `mscz` file and edit the `mscx` file to change or see the channel that an instrument on the stave expects. You may need to ensure that your keyboard is on channel 0.
* [This post](https://musescore.org/en/node/3230010) says that from the mixer you can assign channels to different instruments.

You can use [midi monitor](https://www.snoize.com/midimonitor/) as a lightweight tool to print out midi events. Alternatively your DAW (such as reaper) may have tools to print midi events.

You may need to chang your [midi settings](https://support.apple.com/en-gb/guide/audio-midi-setup/ams875bae1e0/mac).
