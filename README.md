# ThinkPad-T490-EasyEffects-Speaker-Fix
The ultimate EasyEffects preset to transform the ThinkPad T490's notorious "tin-can" speakers into a warm, (maybe) MacBook-style audio experience. Tested on Fedora 43 with KDE Plasma (PipeWire). Eliminates harsh treble and nasal midrange via aggressive V-Cut EQ.

# 1. The Journey: From Tin-Can to MacBook
Like many (or maybe some) ThinkPad T490 users, I was constantly frustrated by the internal speakers. They were tinny, harsh, and the sound felt trapped inside the chassis. The audio lacked body, warmth, and the punch necessary for modern music.

My turning point came after hearing the warm, clear, and spacious soundstage of my friend MacBook. My goal became clear: use the powerful tools available in Linux (specifically EasyEffects) to transform the T490's notorious audio system into something comparable to the smooth, rich output of a MacBook.

This SFSG (So Far So Good) preset is the culmination of weeks of aggressive Equalization tuning and safety testing to achieve that goal (I always test audio with 100% volume lol)

# 2. Technical Philosophy: The Extreme V-Cut
This preset focuses on an aggressive V-Cut strategy, primarily removing the problematic frequencies rather than boosting the weak ones.
Notes: Decrease Input Gain for Equalizer Filter to -3.0 to ensures headroom for the Loudness/Compressor chain.

| Band | Frequency | Final Gain (dB) | Rationale & Result |
| :---: | :---: | :---: | :--- |
| **1** | 30 Hz | -18.0 | **Total Sub-Bass Cut:** Eliminates useless, distortion-causing sub-frequencies (wasteful on T490 drivers). |
| **2** | 60 Hz | -5.0 | **Low Bass Filter:** Cuts problematic low bass, preventing driver stress and boominess. |
| **3** | 119 Hz | +1.5 | **Clean Punch Focus:** Subtle boost for the main body and punch without causing rumbling. |
| **4** | 237 Hz | +1.0 | **Body Definition:** Slight boost to add warmth and definition to instruments. |
| **5** | 474 Hz | -6.0 | **Muddy/Boxy Filter:** Removes low-mid frequencies that cause a "muffled" or "muddy" sound. |
| **6** | 947 Hz | -11.5 | **EXTREME NASAL/TELEPHONE CUT:** Eliminates the primary source of the T490's "tin-can" sound. |
| **7** | 1.8 kHz | -11.5 | **Extreme Harshness Cut:** Removes piercing upper-mid frequencies that cause listener fatigue. |
| **8** | 3.7 kHz | -11.5 | **Harshness Cut (High Mid):** Deep cut to eliminate sharp, fatiguing sounds. |
| **9** | 7.5 kHz | -10.3 | **Treble Smoothing:** Softens sharp high frequencies and sibilance. |
| **10** | 15 kHz | -7.5 | **Air/Detail:** Final cut to eliminate residual harshness at the very top end, while retaining some detail. |

# 3. The Power Chain (Compressor, Loudness, Limiter)
The EQ cuts are balanced by a complex power chain to ensure maximum volume without distortion (clipping):
  1. Compressor: Makeup Gain is set to 0.0 dB to prevent over-boosting of compressed sound. This was the final crucial fix to eliminate vocal "rumbling" on heavy bass tracks (like Billie Eilish's Bad Guy).
  2. Dual Loudness: Two instances of the Loudness filter (+7.0 dB and +4.0 dB) are used to intelligently compensate for the deep EQ cuts, ensuring the sound remains loud and full across all genres.
  3. Limiter (Safety Net):Threshold is set at -0.2 dB to act as a hard safety ceiling. This guarantees that even at 100% volume, the physical speaker drivers will not clip or suffer long-term damage.

# 4. Installation Instructions
  1. Ensure you have EasyEffects installed on your Linux distribution (PipeWire is required). Use EasyEffects from Flatpak with 8.0.5 version or above (I don't know if it working below 8.0.5 version or not, you can try to import it if you want).
  2. Download the SFSG_T490.json file.
  3. Open EasyEffects, go to the Output tab.
  4. Click the Presets button on top left.
  5. Click the Import Preset button, which looks like a document icon with an arrow pointing into it
  6. Load the downloaded SFSG_T490.json file.

_Credit: This preset was developed by Arnaf on a ThinkPad T490 running Fedora 43 with KDE Plasma 6.5.3._
