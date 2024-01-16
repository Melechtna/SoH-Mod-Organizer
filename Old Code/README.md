# Old code

For any developers that would like to understand what I was attempting to do with this old code, so maybe they can fix what I would consider the better way to deal with this.

I tried to make a mod organizer that handles the naming convention the guys over at SoH setup, and after some testing, numerics works just fine with proper padding. For the most part, the difference between the working code, and this broken code, is simply that resorting turned out to be a nightmare, because there were a number of edge cases I couldn't fix without breaking something else, I.E. if a user adds a file, doesn't refresh the list, and hits sort, we should throw up an error and refresh the list.

This version of the code MOSTLY works, but if I recall, the new file prevention doesn't work, and when I tried to impliment it, it broke the listBox again, and started shifting the numbers down from where they currently were on resorting, I.E. 01 would become 42 02 > 42, etc. There's likely a lot of remnants of failed attempts, and file hiding isn't implimented yet either as with the current code base, but those should be the simple parts, as you can basically just take what I did in the current code and slip that straight in.

The current working code is ultimately just a super stripped down version of this code, but with a few things added in to deal with the new focus for the GUI. I also never managed to figure out how to get click drag sorting working for either version of the code, so please, feel free to submit push requests for either version of the code if you can find places to improve!
