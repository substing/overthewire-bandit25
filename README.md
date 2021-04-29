# overthewire-bandit25
 
Another script for an [overthewire Bandit challenge](https://overthewire.org/wargames/bandit/bandit25.html), and this time, level 25. 

The content of the script is honestly made up of something I copied off of a stackoverflow post. I tweaked it a bit, but it is not exactly a totally original work.

The first componet is a for look, simply repeatedly running **echo** with our password and a 4 digit PIN (it will run every possible combination until it finds one which works). After this, it pipes into a **nc** connection, which after connecting will run our for loop.

The final component is that we run **grep -v** to only show the output that does not contain the word "Wrong", so it only will print out what we want: the password. 