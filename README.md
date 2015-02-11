FMDT
====

An IBOC (In-Band-On-Channel) Digital Radio system for FM transmitters.

##Purpose
The purpose of *FMD (FM-Digital)*, is to provide an open alternative to Ibiquity's *HD Radio* system for hobbyists and low-power broadcasters.

##Prequisites
I have yet to write DRM30 modulation blocks for the graph and thus, for this implementation we will use *Dream*. On most Linux systems, the following is all you will need to get started:
- GNURadio 3.7 or later.
- JACK Audio Connection Kit (Jackd2)
- gr-drm https://github.com/kit-cel/gr-drm
- (Optional) Stereo Tool or Breakaway Broadcast Processor

##What it does.
FMDT is, simply put: "Kind of like HD Radio, except it uses DRM (Digital Radio Monodale) signals as opposed to Ibiquity's proprietary OFDM scheme and codecs. It is intended to give FM stations digital capabilaties of similar or better qualliy than what current commercial standards allow. Occupying a total bandwidth of ~300khz (150khz deviation), it is both bandwidth-efficient, as well as mindful to traditional analog standards. 

Standards used for this system:
-  NRSC-5-C (National Radio Standards Commitie)
-  ITU-R SM.1268 (FM Composite clipping standards)

====
#TODO
- Implement a DRM30 (Robustness mode A) transmitter with multi-service capabilaty in GNURadio
- 

====
# BLADERF FORUM THREAD

##Hybrid Digital FM Transmitter
Here is a project I have been working on for some time now -- a DRM (DDigital Radio), and FM (Stereo) transmitter "inspired" by HD Radio. Using JACK, you can send both standard analog and digital radio with the BladeRF. The digital decodes in Dream, and the FM works perfectly on every receiver I have tested. Instructions on how to use after the screenshots.

##Download & Use
- Compile gr-drm and ensure it is working by running the flowgraphs as explained in its readme.
- Be sure your config.conf has the following in it:

```sh
[audio]
audio_module = jack
```

