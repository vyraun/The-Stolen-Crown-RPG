The Stolen Crown: A mini-RPG
====================

A fantasy mini-RPG built with Python and Pygame.

Requirements: Python 2.7, Pygame 1.9.1

How to run: python The_Stolen_Crown.py

Video Demo: https://www.youtube.com/watch?v=MkZXaDQfTSo


![screenshot](https://raw.github.com/justinmeister/The-Stolen-Crown-RPG/master/screenshot.png)

![screenshot #2](https://raw.github.com/justinmeister/The-Stolen-Crown-RPG/master/screenshot-2.png)

King's Theme by Telaron: opengameart.org/content/the-kings-crowning

Town Theme by Mekathratos: opengameart.org/content/danza-del-bosque

Overworld Theme by bart: opengameart.org/content/adventure-begins

Shop Theme by Aaron Krogh: https://soundcloud.com/aaron-anderson-11/a-4-coastal-town

Victory Theme by matthew.pablo http://opengameart.org/content/enchanted-festival

#Error

http://pygame-users.25799.x6.nabble.com/pygame-image-get-extended-0-Tried-everything-should-I-just-give-up-td1854.html

OK - good news! Finally! 
It turns out that the libpng and libjpeg that are in Anaconda are not appropriate for pygame. This I found out from a post in their page. 

There is a work around - I used it - and now I can say that Pygame works for me with the extended image control. 

This took some time, but I think, now that it's coming to an end, a good learning experience. 

I want to thank those who kindly took their time to suggest ideas.

> It turns out that the libpng and libjpeg that are in Anaconda are not appropriate for pygame. This I found out from a post in their page.

This kind of thing (which I've also seen with Anaconda's Qt libraries under Linux) is why I tend to avoid it, though I know quite a few people are happy with it, and it's nice to have something consistent across platforms with pre-built binaries, which I think is a USP for Anaconda. On OS X/Linux it also avoids installations into /usr/local (or worse /usr) and doesn't require sudo, which is good for centrally managed systems.

This comes from the Anaconda support help that I got. I cannot take credit for this solution, only for seeking it out and passing it on!

brew install sdl sdl_image sdl_mixer sdl_ttf portmidi 

conda install -c https://conda.binstar.org/quasiben pygame 

There apparently is some issue between the libjpeg and libpng that comes with anaconda (where is it run) and those that you will compile with if you compile pygame, as I did many times. The conda install command actually will install a pygame that was compiled to work with those libraries in anaconda so that when you actually run things, you will get the extended image support.
	
The first line requires that you have brew installed and it will install the SDL packages and portmidi. The second line uses conda - the equivalent of brew, but in anaconda. This will actually take the SDL and port midi that was installed, and use it as a dependency for the pygame. 

This is apparently a 64 bit installation. I found that it worked just fine for me. So now I have the comfort of anaconda, and the availability of pygame - which is exactly what I wanted. 

I hope this helps out.
