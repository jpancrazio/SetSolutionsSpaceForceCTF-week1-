# Uniform Fashion

In this challenge, we are presented with the following clue:
[picture](/Uniformity1.png)

Since this seemed like a starighforward steganography challenge, I started with the basics. First, I ran exif to see if there was anything obvious hiding.
No luck.
After that, I gave binwalk a shot, using the extract and matryoshka options. Matryoshka is basically a recursive extraction.
Still no luck.
Steghide was my next tool of choice, which showed me that something is hiding in the file. I tried many variations of FLOTUS and Melania(Trump) for the passphrase, but was never successful. (Even after solving this challenge, I tried using the flag to open this file to no avail. Maybe it was just a red herring?)
[picture](/Uniformity2.png)

I decided to try visually inspecting the file a little closer and felt rather silly when I found the flag in plain view, listed as the author of the file.
[picture](/Uniformity3.png)
