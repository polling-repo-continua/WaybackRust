WaybackRust
===

WaybackRust is a tool written in Rust to query the [WaybackMachine](https://archive.org/web/).

Here is the functionalities : 
* Get all urls for a specific domain and get their current HTTP status codes.
* Get all link in the robots.txt file of every snapshot in the WaybackMachine.

## Install 

##### from cargo (crates.io):
`cargo install waybackrust`

##### from github:
* Clone this repository `git clone https://github.com/Neolex-Security/WaybackRust`  
* `cargo build --release`
* The executable is in : `./target/release/waybackrust`

## Usage

```
waybackrust 0.1.1
Neolex <hascoet.kevin@neolex-security.fr>
Wayback machine tool for bug bounty

USAGE:
    waybackrust [SUBCOMMAND]

FLAGS:
    -h, --help       Prints help information
    -V, --version    Prints version information

SUBCOMMANDS:
    help      Prints this message or the help of the given subcommand(s)
    robots    Get all disallowed entries from robots.txt
    unify     Get the content of all archives for a given url
    urls      Get all urls for a domain


```
###### Urls command :
```
waybackrust-urls 
Get all urls for a domain

USAGE:
    waybackrust urls [FLAGS] <domain>

FLAGS:
    -h, --help       Prints help information
    -n, --nocheck    Don't check the HTTP status
    -s, --subs       Get subdomains too
    -V, --version    Prints version information

ARGS:
    <domain>    Get urls from this domain

```

###### Robots command :
```
waybackrust-robots 
Get all disallowed entries from robots.txt

USAGE:
    waybackrust robots <domain>

FLAGS:
    -h, --help       Prints help information
    -V, --version    Prints version information

ARGS:
    <domain>    Get disallowed urls from this domain
```

###### Unify command : 
```
waybackrust-unify 
Get the content of all archives for a given url

USAGE:
    waybackrust unify [OPTIONS] <url>

FLAGS:
    -h, --help       Prints help information
    -V, --version    Prints version information

OPTIONS:
    -o, --output <FILE>    name of the file to write contents of archives

ARGS:
    <url>    The url you want to unify
```
## Ideas of new features
If you have idea of improvement and new features in the tool please create an issue or contact me.