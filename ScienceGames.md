#Science Games

In this challenge, we are presented with some simple instructions: "Connect to the range at 18.224.78.17 port 1337" along with a great hint.

![picture](https://github.com/FredMFNRogers/SetSolutionsSpaceForceCTF/blob/main/ScienceGames1.png?raw=true)

The first tool that came to mind was netcat, so I used that to connect to the IP and port in question. From here, I was presented with a string of emojis proceeded with what appeared to be a dictionary.

![picture](https://github.com/FredMFNRogers/SetSolutionsSpaceForceCTF/blob/main/ScienceGames2.png?raw=true)

After using the dictionary to decode the message shown (I did this manually although I'm sure it could be scripted as well), I was left with a string of base 16 numbers. When translated into ASCII, this encoded text yielded the message "Send back S to get next character".

![picture](https://github.com/FredMFNRogers/SetSolutionsSpaceForceCTF/blob/main/ScienceGames3.png?raw=true)

After entering "S" and hitting enter when connected via netcat, I was presented with the same message. I thought I must have done something wrong and just hit enter again. This time, however, an error message was displayed. This got me thinking I was on the right track after all.

![picture](https://github.com/FredMFNRogers/SetSolutionsSpaceForceCTF/blob/main/ScienceGames4.png?raw=true)![picture](https://github.com/FredMFNRogers/SetSolutionsSpaceForceCTF/blob/main/ScienceGames5.png?raw=true)

This time, after entering "S" the first round, I entered "S" again. This time, the message was the exact same again... except for one character: the "S" I was asked to return was replaced with an "I". I was on to something!!

![picture](https://github.com/FredMFNRogers/SetSolutionsSpaceForceCTF/blob/main/ScienceGames6.png?raw=true)

About two dozen rounds of this later and I had compiled a flag and was awarded with a congratulatory message.

![picture](https://github.com/FredMFNRogers/SetSolutionsSpaceForceCTF/blob/main/ScienceGames7.png?raw=true)
