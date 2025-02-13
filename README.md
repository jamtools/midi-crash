# MidiCrash

Use your crash cymbal as a midi controller!

In order to use this, you can put a [drum trigger](https://www.sweetwater.com/store/detail/DDT--drumdial-drum-trigger-with-clip-mount) on your cymbal stand (rather than the cymbal itself), plug the drum trigger into your computer through an audio interface or something cheaper like [this](https://www.amazon.com/6-35mm-Plated-Interconnect-Shelled-Adapter/dp/B07VGF7DJV).

Then:
- Download [JACK Audio](https://jackaudio.org) and configure it to use your intended audio input
- Download [Go](https://github.com/jamtools/midi-crash/blob/master/jack-peak-meter.go)
- Clone this repo and run `go mod tidy`
- Run `go run jack-peak-meter.go`.

This is based off of an existing tool that shows a volume meter of an audio input https://github.com/gethiox/jack-peak-meter. Modifications were done [here](https://github.com/jamtools/midi-crash/pull/1/files) to make the MIDI functionality work.

Thank you [@gethiox](https://github.com/gethiox)! I like the original README and it's staying here:

---

# ULTIMATE SOUND VISUALIZER 2,000,000

Welcome!  
Well, it's not as ultimate as it could be but also it's not so bad so far.

![visualizer animation](/doc/animation.gif)

# Requirements

`ULTIMATE SOUND VISUALIZER 2,000,000`® uses [JACK Audio Connection Kit](http://jackaudio.org/) as base sound system,
if you are using Ubuntu or another distribution with PulseAudio I have good news for you — You even don't need to
download this piece of script on your computer. I made it for myself as my first attempt into [Go](https://golang.org/)
programming language.  
Code uses [xthexder](https://github.com/xthexder)'s [go-jack](https://github.com/xthexder/go-jack) library/bindings for JACK Audio Connection Kit.  

# Usage

    ./jack-peak-meter -title
    
# Build

    go build jack-peak-meter.go
    
