---
layout: post
title: The First Post
---

As you've probably noticed, the Patreon campaign is over. Many thanks to all supporters
for their kind support! Without your support, Aedict wouldn't be so advanced as it is now.
However, I came to a realization that Patreon is not the way to make money.
I will therefore be closing the Patreon account and canceling all support pledges.

This however does not mean that Aedict is dead. I am definitely not giving up :)
What I'm going to try next is to make the basic features of Aedict 3 available for free,
locking out advanced features behind a recurring payment via Google Play.
This way, the users can directly support Aedict via Google Play; this move will
also protect against the piracy. I have no idea whether this move will yield
more sustainable income, we have to jump the ship and see.

Currently the progress is behind-the-scenes: I finally succeeded in finding a
replacement for the aging way of storing your notepad and tags. It's not CouchBase Lite -
[that's a piece of junk](http://mavi.logdown.com/posts/7425397) and it will go away.
If you tried to use it please switch to the File-based database while the new way
is implemented. The new [UMN Database](https://gitlab.com/mvysny/umn) is still in alpha and the documentation is sketchy,
but it's based on a rock-solid and blazingly-fast [H2 MVStore](http://www.h2database.com/html/mvstore.html).

Android mandates that all app updates must support the runtime permissions,
so I'm going to work on that next. That's a lot of changes under the hood,
and given Android fragmentation, I'm sure it's going to crash a lot :-D
Stay tuned, and thanks!
