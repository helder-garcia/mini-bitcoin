# Mini Bitcoin - Simple cryptocurrency
> Minimal Bitcoin Protocol in Java (Satoshi White Paper, not Bitcoin Core)

## Description
Just small 8 files. Standard Java Library. No JARs.

Wallet(Private and Public keys), Blockchain, Miner, P2P (Server and client), RPC(http).. all ready.

Our goal is to decentralize the power of creating currencies. 

There are about 10 million of Java programmers around the world.

Currencies must compete in the market, like any goods or services. 

Fork this. Create your own cryptocurrency!

[Bitcoin White Paper](https://bitcoin.org/bitcoin.pdf)

## How to GO
* Download [Eclipse IDE](https://www.eclipse.org/downloads/)

* Clone or fork this repository.

* Eclipse File->New->Java Project (copy files inside when ready)

## Understanding the code
Inside mbtc.Main you get the "main method" starting point.

Run and go to http://localhost:8080/

You can try put a breakpoint in the first line 

```
* K.SEEDS[0] = "localhost";
```

and go debugging too. :-)

No threadssss, just ONE execution line.

## Docker
Start two nodes to check how the peers exchange messages. 

WARNING: 
* Clean Blockchain/KeyPair/UTXO folders before build.
* UNCOMMENT this line in Main.java

``` 
 K.SEEDS[0] = "localhost";
```

You can run just one docker(peer) and then run in Eclipse another peer to easily debug.

```
docker build -t mbtc .
docker run -it -p 10762:10762 --rm mbtc
```
Or use docker-compose to run two peers

WARNING:
* Clean Blockchain/KeyPair/UTXO folders before build. 
* COMMENT this line in Main.java

``` 
// K.SEEDS[0] = "localhost";

$ docker-compose build
$ docker-compose up
```

## What is address?
It's just a shortcut to the public key. Once your public key is on the blockchain, you will receive coins using small 
address, instead of use the large public key.

Example: 

```
publicKey: MFYwEAYHKoZIzj0CAQYFK4EEAAoDQgAEiCEOTeXDzM8lDlj21vmzQxzu9w6aN8f98uq3fSBwBQtL627QBvH0Rk8xsT9leiYtByp815SNPEcxS0cFXEm4IA==

address: 4d744-2
```
You can use (to send 1 mbtc):

```
/send 1 4d744-2 
```

Or (IF the publickey is not in the blockchain yet.)

```
/send 1 MFYwEAYHKoZIzj0CAQYFK4EEAAoDQgAEiCEOTeXDzM8lDlj21vmzQxzu9w6aN8f98uq3fSBwBQtL627QBvH0Rk8xsT9leiYtByp815SNPEcxS0cFXEm4IA==
```

More than 4 billions of possible addresses.

## Help

If you need my help, don't hesitate to ask me.

[My twitter](https://twitter.com/_oliberal)

Enjoy!