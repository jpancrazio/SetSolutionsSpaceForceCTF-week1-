# Secret Squirrel

This challenge included a document to download and inspect named "hidden.docx". 

![picture](https://github.com/FredMFNRogers/SetSolutionsSpaceForceCTF/blob/main/SecretSquirrel1.png?raw=true)

Upon opening this file in LibreOffice, I could see that there was text set to the same color as the background. I changed the font color and was able to pull the message "There is more to this document than meets the eye." After running through exif, steghide, and binwalk with no success, I opened the file in archive manager and noticed it was compressed.

![picture](https://github.com/FredMFNRogers/SetSolutionsSpaceForceCTF/blob/main/SecretSquirrel2.png?raw=true)

After extracting the file, in one of the hidden folders, I saw a file named "extra". After cat'ing "extra" I was presented with the flag.

![picture](https://github.com/FredMFNRogers/SetSolutionsSpaceForceCTF/blob/main/SecretSquirrel3.png?raw=true)
