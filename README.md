# Bruh, im tired hearing this "tin-can" T490 speakers on Linux, so i decided to...
Make EasyEffects preset and transforming my ThinkPad T490's notorious "tin-can" speakers into a warm, (maybe) MacBook-style audio experience. Tested on Fedora 43 with KDE Plasma (PipeWire). Eliminates harsh treble and nasal midrange via aggressive W-Cut EQ.

# 1. The Journey: From Tin-Can to MacBook
Like many (or maybe some) ThinkPad T490 users, I was constantly frustrated by the internal speakers. They were tinny, harsh, and the sound felt trapped inside the chassis.

My turning point came after hearing the warm, clear, and spacious soundstage of my friend MacBook. My goal became clear: use the powerful tools available in Linux (this time i choose EasyEffects) to transform the T490's notorious audio system into something comparable to the smooth, rich output of a MacBook.

This T490_Clear_Audio_Fix.json preset is the culmination of weeks of aggressive Equalization tuning and safety testing to achieve that goal (I always test audio with 100% volume lol)

# 2. Technical Philosophy: The W-Cut
This preset focuses on an W-Cut strategy, primarily removing the problematic frequencies (especially EQ bands that making Thinkpad T490 sounds like tin-can or in a telephone / nasal) rather than boosting the weak ones. 

# 3. The Power Chain (Compressor, Loudness, Limiter)
The EQ cuts are balanced by a simple power chain to ensure maximum volume without distortion (clipping):
  1. Compressor
  2. Loudness
  3. Limiter

# 4. Installation Instructions
  1. Ensure you have EasyEffects installed on your Linux distribution (PipeWire is required). Use EasyEffects from Flatpak with 8.0.5 version or above (I don't know if it working below 8.0.5 version or not, you can try to import it if you want).
  2. Download the T490_Clear_Audio_Fix.json file.
  3. Open EasyEffects, go to the Output tab.
  4. Click the Presets button on top left.
  5. Click the Import Preset button, which looks like a document icon with an arrow pointing into it
  6. Load the downloaded T490_Clear_Audio_Fix.json file.

# 5. Community & Contribution
This preset is a starting point, born from personal frustration and experimentation. The values are optimized for my specific T490 unit and my personal taste (MacBook style).

**You are highly encouraged to:**
1.  **Experiment Further:** Feel free to tweak the EQ values (especially the aggressive V-Cuts) to fit your own speakers and preferences.
2.  **Contribute Back:** If you find an improvement, share your findings!

If you want to suggest a change, discuss a new feature (like a Stereo Tools configuration), or share a successful tweak for another ThinkPad model:
* Please open a **GitHub Issue** detailing your proposed change or finding.
* If you create a modified `.json` file, feel free to open a **Pull Request**!

_Credit: This preset was developed by Arnaf on a ThinkPad T490 running Fedora 43 with KDE Plasma 6.5.3._
