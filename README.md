# Command-line Upload Script

An upload script for the command line with zip and random name option.


## Installation

First we will create a ~/bin folder in your home directory.

`mkdir ~/bin/`

After that we need to open the file `~/.bash_profile` and add the following to the top.
`export PATH="$HOME/bin:$PATH"`


**Info:** The `export PATH=` contains all the directories that will be looked into for executable binaries when you type a command in Terminal.


Since we changed the `~/.bash_profile` file we now need to quickly reload it with the following command:
```sh
source ~/.bash_profile
```


Now we only need to copy our `upl` file into the ~/bin folder `cp /path/to/file/upl ~/bin/upl` and set the permissions 
`chmod u+x ~/bin/upl`.


### Config

```sh
hostname="domain.de"
user="root"
password=""
path="/path/to/public/directory/"
```

**We are ready to go!**


## Usage

_It is pretty easy to use the tool:_


`upl [filename] -z [optional] -r [optional]`



Options:

`-z` this option will zip your file

`-r` this option will give your file a random name

use `-z -r` to create a zipped file with a random name




## Dev

- put link to file in clipboard
- directory support
