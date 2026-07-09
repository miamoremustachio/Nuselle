# 🎵 Basics

To handle digital audio, modern computers use method called *PCM*.
PCM stands for Pulse-code Modulation, which is a way to represent sampled analog signals in a digital format.

For PCM to be converted into an analog signal, you need a DAC (**D**igital to **A**nalog **C**onverter), which is usually performed by a sound card.

A PCM stream has two basic properties: the *sampling rate* and the *bit depth*.

The sampling rate is expressed in Hz and determines how often a sample of a waveform is captured; while the bit depth determines the number of bits of information in each sample.

# 🎶 Resampling

*Resampling* is the process of turning a PCM stream into another PCM stream of a different resolution.

# 💿 Encoding

*Encoding* is the process of taking a PCM stream and writing it to a permanent format.

Audio codecs used for encoding can be either *lossy* (MP3, OPUS) or *lossless* (FLAC, ALAC, WAV).
Lossy encoding removes data from the PCM stream to safe space, while lossless encoding takes a PCM stream and converts it in such a way that no data is lost.

A new property encoding brings is the *bit rate*, which determines the amount of data processed per time unit, measured in kilobits per second (kbps)

# 💃 ALSA






[^1]: Sources:
	https://www.reddit.com/r/linux/comments/coi4dt/a_complete_guide_of_and_debunking_of_audio_on/
