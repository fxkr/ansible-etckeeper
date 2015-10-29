# ansible-etckeeper

An ansible module that makes it easier to keep a
log of changes in /etc via etckeeper.

Author: `Felix Kaiser <felix.kaiser@fxkr.net>`  
License: revised BSD (see LICENSE)  
Version: 1.0.0  


## Current state (Oct 2015)

Caveat emptor, but I'm using it in production.


## How to use

See EXAMPLES section in the module, but you basically just put

```
- etckeeper: action=begin
```

at the beginning of your plays and

```
- etckeeper: action=commit msg="foo"
```

at the end of your plays.


## How well does it work?

Pretty well, as long as plays are kept relatively short.

The main problem is the interaction with ansible tags.

