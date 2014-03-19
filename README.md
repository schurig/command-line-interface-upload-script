# Command-line Upload Script

An upload script for the command line with zip and random name option.


# Installation

1) **First you will need to clone this repository to your local machine:**
you can choose the location where you want to put it, just remember where you put it because we will need the path in one of the next steps

`git clone git@github.com:schurig/command-line-upload-script.git`


2) If you don't have it yet, we will now create a **~/bin** folder in your home directory:

`mkdir ~/bin/`

3) After that we need to open the file `~/.bash_profile` and add the following to the top:

`export PATH="$HOME/bin:$PATH"`

5) Just **restart your terminal** because we changed the `~/.bash_profile` file and it needs to reload.


>By the way, the `export PATH=` contains all the directories that will be looked into for executable binaries when you type a command in your Terminal. We do this so that we later on can easily run the `upl` command.



6) Now we only need to create a symbolic link of our `upl` file and place it into our **~/bin** that should be in your home directory:

```sh
ln /path/to/repository/upl ~/bin/upl
```


5) and set the right permissions: 

`chmod u+x ~/bin/upl`.


# Configuration

Open the  `upl` file and customise the settings:

```sh
hostname="domain.de"
user="root"
password=""
path="/path/to/public/directory/"
```


# Usage

_It is pretty easy to use the tool:_


`upl [filename] -z (optional) -r (optional) -s (optional)`



Options:

`-z` this option will zip your file

`-r` this option will give your file a random name

`-s` this option will shorten your link


###examples:

```sh
upl 1337.jpg -z -s
```

>Uploading the file **1337.jpg.zip** to the server. The URL will be shorten and the zip file contains your picture **1337.jpg**



# What I am still working on

- put link to file in clipboard
- directory support
