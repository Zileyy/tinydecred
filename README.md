# TinyDecred

A Python 3 Decred toolkit. The modules in TinyDecred can be used to integrate 
Decred into Python projects. Everything needed to create wallets to send and
receive DCR.

## Features

1. Pure-Python secp256k1 elliptical curve.

1. Serializable and de-serializable python versions of important types
from the dcrd/wire package: `MsgTx`, `BlockHeader`, `OutPoint`, etc. 

1. BIP-0044 keys. Account creation and management. PGP mnemonic seeds. 

1. Network parameters for mainnet, testnet3, and simnet. 

1. Clients for the dcrdata block explorer API (websockets, pubsub, HTTP). 

1. Experimental PyQt5 light wallet. 

## Installation

Install by cloning the git repo. 
The `tinydecred` directory or a symlink will need to be in `PYTHONPATH`. 

All dependencies are available through PyPi.

```
sudo pip3 install PyQt5==5.9.2 websocket_client blake256 base58 pynacl appdirs
```

though depending on your setup, you may or may not need `sudo`, and `pip3` might
be simply `pip`. 

You're probably okay with newer versions of PyQt5, but `5.9.2` has been 
remarkably stable.

## Wallet

TinyDecred is the name of the package as well as the experimental light wallet
GUI application. 
**The light wallet is experimental, and should not be used on mainnet.**

To start the wallet, navigate to the `tinydecred` package directory, and run

```
python app.py --testnet
```

The wallet runs as a system-tray application, of which the major difference is 
that "closing" the wallet actually just removes the entry from the taskbar and
minimizes the window "to the system tray". 
The wallet can then be "opened" again through the icon in the system tray. 

![alt text][screenshot]

TinyDecred is pretty small.
Like Decred, it's meant to be an omnipresent yet largely invisible and 
unobtrusive part of your digital environment. 
The small dialog size keeps user interactions focused.
Bells and whistles are minimized in favor of simplicity whenever possible.
Blockchain mechanics are invisible. 
The goal is to make using Decred easier than pulling change out of your pocket.

## Roadmap

In no particular order 

- Staking
- Schnorr signatures and Edwards curve
- SPV Node
- Bitcoin accounts
- Decred DEX integration
- Lightning network

[screenshot]: https://user-images.githubusercontent.com/6109680/62095772-08b4ce80-b247-11e9-81ae-66931ebb07be.png






