---
cssclasses:
  - banner
  - banner-fade
---
![[VLC-media.png|banner]]
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

## If the above doesn't help

 \> Tools
 \> Preferences
 \> All
\> Input/Codecs
\> Advanced
\> Set *File caching (ms)* and *Disc caching (ms)* to `111`
 


