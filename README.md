# Command line interface Upload Script (cli)

An upload script for the command line interface that supports:
- zipping
- short urls (goo.gl)
- auto-copy to clipboard
- random names


# Installation

1) First you will need to clone this repository to your local machine:


`git clone git@github.com:schurig/command-line-upload-script.git`

You can choose the location where you want to put it, just remember where you put it because we will need the path in one of the next steps.



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
# Settings
hostname="domain.tld"; # the hostname of your server (ip also works)
user="user"; # the username that you would like to login to on your server
password=""; # your password for your server (not needed in case you use ssh-keys)
path="/path/to/public/directory"; # the directory on the server that the files get uploaded to
url_to_path="http://domain.tld/"; # public domain where you can view/download the files

RANDOMIZE_NAME=false; # randomize the filename by default
ZIP=false; # zip by default
URL_SHORTEN=true; # shorten by default
COPY_TO_CLIPBOARD=true; # copy link to clipboard by default
```


# Usage

_It is pretty easy to use the tool:_


`upl [filename] -z (optional) -r (optional) -s (optional) -c (optional)`



Options:

`-z` this option will zip your file

`-r` this option will give your file a random name

`-s` this option will shorten your link

`-c` this option will copy the link to your clipboard



###Examples:

```sh
upl 1337.jpg -z -s -c
```

>Uploading the file **1337.jpg.zip** to the server. The URL will be shorten and the zip file contains your picture **1337.jpg**. The public link to the zip file will be ready to paste in your clipboard.



# What I am still working on

- custom public and private ssh-keys
- ftp support
- multible file support

* eating as many cookies as possible with just one byte
