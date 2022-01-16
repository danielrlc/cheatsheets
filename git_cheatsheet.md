Git cheatsheet
==============

Branches
================================================================================

git checkout -   | Toggle between last two branches git fetch origin           |
Fetch branches from remote repository git checkout mosaico/more-ads | Checkout
mosaico/more-ads branch


Chat with Fabrizio (tidy up at some point)

Just to recap, are these all the steps needed to pull and set up a new branch
locally?

git fetch origin git checkout mosaico/more-ads


Fabrizio's advice:

Yes! You can shorten the first one to just git fetch when you want to fetch from
origin 12:11

And you can replace it with git pull if you want the latest changes
from the remote branch incorporated in your current branch 12:11 (fetch will
just download the changes locally but not apply them.

I usually do git pull
unless I need to do some reshuffling with commits)

