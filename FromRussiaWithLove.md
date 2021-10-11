# From Russia With Love

In this challenge, I was given the sign-in form below. I could see that in order to sign in as Yuri, I would need to have a username, password, and TOTP.

![picture]()

The attached file was a picture of a post-it note that contained a string denoted as TOTP secret. 

![picture]()

Without that prior tidbit of knowledge, the first thing I decided to do here was to try some simple SQL injection techniques to sign in as admin or to enumerate any underlying database tables. As you can see below, that didn't qork out how I wanted.

![picture]()

At this point, I inspected the source code and was able to find a username and password. So now I had all three components needed to sign in... or so I thought.

![picture]()

