# From Russia With Love

In this challenge, I was given the sign-in form below. I could see that in order to sign in as Yuri, I would need to have a username, password, and TOTP.

![picture](https://github.com/FredMFNRogers/SetSolutionsSpaceForceCTF/blob/main/FromRussiaWithLove1.png?raw=true)

The attached file was a picture of a post-it note that contained a string denoted as TOTP secret.

![picture](https://github.com/FredMFNRogers/SetSolutionsSpaceForceCTF/blob/main/FromRussiaWithLove2.png?raw=true)

The first thing I decided to do here was to try some simple SQL injection techniques to sign in as admin or to enumerate any underlying database tables. As you can see below, that didn't work out how I wanted.

![picture](https://github.com/FredMFNRogers/SetSolutionsSpaceForceCTF/blob/main/FromRussiaWithLove3.png?raw=true)![picture](https://github.com/FredMFNRogers/SetSolutionsSpaceForceCTF/blob/main/FromRussiaWithLove4.png?raw=true)

At this point, I inspected the source code and was able to find a username and password. So now I had all three components needed to sign in... I just didn't realize what to do with them quite yet.

![picture](https://github.com/FredMFNRogers/SetSolutionsSpaceForceCTF/blob/main/FromRussiaWithLove5.png?raw=true)

Initially I tried to use the TOTP secret found on the post-it note as the MFA code for Yuri's login which seemed like a very complex TOTP, but that was not correct. After sleeping on it and reading some write-ups from others on similar challenges, I had the epiphony that the TOTP secret I possessed was actually a seed. After inputting the seed into a TOTP generator and waiting for the code to refresh, I was able to successfully sign in as Yuri and claim my flag!

![picture](https://github.com/FredMFNRogers/SetSolutionsSpaceForceCTF/blob/main/FromRussiaWithLove6.png?raw=true)![picture](https://github.com/FredMFNRogers/SetSolutionsSpaceForceCTF/blob/main/FromRussiaWithLove7.png?raw=true)
