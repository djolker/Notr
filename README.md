#Notr

Notr is a Java command line application that allows you to manage quick notes.  This program
is mainly meant to be used with the program Conky as a means to print out the
notes.  Notr is very much inspired by the note taking tool from the hacking
simulator "HackNet"

Requirements
------------
* Java

Installation
------------

Clone from git:
```sh
git clone https://github.com/djolker/Notr.git
```

Run the install script as root:
```sh
sudo sh install.sh
```

Usage
-----

notr command [args]

  Commands:

    read                            Lists notes with flare written on it

    write                           Prompts the user for the new note

    erase [index of note to erase]  Removes the Note that matches index with
                                    the one provided by the user

Conky Usage
-----------

Adding a line in Conky to integrate Notr is pretty simple. In order to avoid
text cutting off, it's recommended you use the fold command to start word wrap
in the Notr session.

Example:

```sh
${execpi 5 notr read | fold -sw 63}
```
