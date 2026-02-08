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
\> **Pulseaudio audio output**

*finally:*

\> Tools
\> Preferences
\> All
\> Input/Codecs
\> Advanced
\> Set *File caching (ms)* and *Disc caching (ms)* to `50`
 


