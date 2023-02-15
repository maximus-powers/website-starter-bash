# Website Starter Bash Script

Originally published on [Medium](https://medium.com/@maximuspowersdev/website-starter-bash-script-9cc95e7d67f2)

I hate to admit it, but every time I start coding a new website, I start from scratch. It's time to change that.
Normally I'd create a empty folder, add a few new files (e.g. index.html, style.css, and script.js), and spend 10 minutes typing out the HTML scaffolding for my site. 
In this post, I'll be building a bash script (run from the CLI), that automates this process so I can skip straight to building out the site.

---

## What is a Bash Script

Normally, I run a few commands from the CLI to create the directory and files I need for a website. The thing is, I run the same commands every single time. Putting all of these commands in one place (the bash script) allows me to run them all with just one command. 

For more information check out [this article](https://ryanstutorials.net/bash-scripting-tutorial/bash-script.php) by Ryans Tutorials.

---

## Writing the Script

1. First things first, create a file called bashscript.sh


2. Start the script off with a shabang ('#!') and define the path to the bash shell

`#!/bin/bash`


3. Prompt user to give the website's directory a name

`echo "Enter the name of the website:"
read website`


4. Create a directory with that name, then change directory so the bash script will execute inside of it

`mkdir ~/Desktop/$website
cd ~/Desktop/$website`


5. Create the starter files

`touch index.html
touch style.css
touch script.js`


6. Add a boilerplate to the index.html file. The boilerplate included in this repo contains:
 - Bootstrap CDN links
 - Basic framework for HTML items (e.g. nav, header, main, footer)
 - JS and CSS files from the directory
 
 
7. Print a message to the command line, confirming the website starter has been created

`echo "Website folder and starter files have been created!"`

---

## Running the Script

1. First you need to compile the script with this command

`chmod u+x bashscript.sh`


2. To run it, make sure you're in the same directory as the script, then type:

`./bashscript.sh`


3. You'll be asked to name the directory, then you're done! You'll find it on your desktop, ready to be built out.

---

## Conclusion

I've already used the script to start a couple new projects, and it makes a big difference. It saves only saves me about 10 minutes of pulling together links, scaffolding, and tedious tasks, but the real advantage is avoiding the headache. 
