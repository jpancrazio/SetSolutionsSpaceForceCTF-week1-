# Uniform Fashion

In this challenge, we are presented with the following clue:
![picture](https://github.com/FredMFNRogers/SetSolutionsSpaceForceCTF/blob/main/Uniformity1.png?raw=true)

Since this seemed like a starighforward steganography challenge, I started with the basics. First, I ran exif to see if there was anything obvious hiding.
No luck.
After that, I gave binwalk a shot, using the extract and matryoshka options. Matryoshka is basically a recursive extraction.
Still no luck.
Steghide was my next tool of choice, which showed me that something is hiding in the file. I tried many variations of FLOTUS and Melania(Trump) for the passphrase, but was never successful. (Even after solving this challenge, I tried using the flag to open this file to no avail. Maybe it was just a red herring?)
![picture](https://github.com/FredMFNRogers/SetSolutionsSpaceForceCTF/blob/main/Uniformity2.png?raw=true)

I decided to try visually inspecting the file a little closer and felt rather silly when I found the flag in plain view, listed as the author of the file.
![picture](https://github.com/FredMFNRogers/SetSolutionsSpaceForceCTF/blob/main/Uniformity3.png?raw=true)
