# cmorse
[![The MIT License](https://img.shields.io/badge/license-MIT-orange.svg?style=flat-square)](http://opensource.org/licenses/MIT)
[![Travis CI](https://img.shields.io/travis/Jacajack/cmorse.svg?style=flat-square)](https://travis-ci.org/Jacajack/cmorse)

`cmorse` is a simple text to Morse code converter

[Cmorse on launchpad...](https://launchpad.net/cmorse)

![Screenshot](http://i.imgur.com/Xy3KEZW.gif)
<br>*Screenshot of v1.0* &nbsp;&nbsp;&nbsp;&nbsp;<sup><sub>*That chameleon, tho...*</sub></sup>

## Installing cmorse
 - Add PPA to your system - `sudo add-apt-repository ppa:mrjjot/cmorse`
 - Update software lists - `sudo apt-get update`
 - Install `cmorse` package - `sudo apt-get install cmorse`


## Usage
`cmorse [OPTIONS]`

Supported command line options:
 - `-h` / `--help` - Display help message
 - `-v` / `--version` - Display software version number
 - `-i` / `--input` - Specify input file in next argument
 - `-o` / `--output` - Specify input file in next argument
 - `-d` / `--decrypt` - Convert from Morse code to regular text
 - `-u` / `--uppercase` - Output uppercase text, when decrypting
 - `-p` / `--prosginsdisabled` - Disable automatic prosign insertion (like `.-.-` instead of new line)

For example, `cmorse -i example.txt -o example.morse` will encode `example.txt` and store Morse code in `example.morse`.
To reverse process use `cmorse -d -i example.morse -o decrypted.txt`.

When input file is not specified, `cmorse` will read `stdin` until `EOF` or `EOT` character occurs.
Same applies to output files - when not specified, `cmorse` will write to `stdout`.

## Building from source
 - Clone git repository - `git clone https://github.com/Jacajack/cmorse.git && cd cmorse`
 - Invoke makefile - `make all`
 - To install use `sudo make install`, and to uninstall - `sudo make uninstall`.
