# 🔉 Fix sound stuttering issue

 \> Tools
 \> Preferences
 \> All
 \> Audio
 **❌** Enable time stretching audio

*then:*

\> Output modules
\> Audio output module
\> **ALSA audio output**

*finally:*

\> ALSA
\> Audio output device
\> Select audio card("Direct hardware device without any conversions")

*to find your sound card:*
```bash
sudo aplay -l
```


