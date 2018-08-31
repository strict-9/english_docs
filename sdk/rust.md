## RUST version of the SDK

The source code is located at: https://github.com/trustnote/rust-trustnote/archive/0.3.0.zip

The executable files for both operating systems are currently compiled:

Ubuntu

Https://github.com/trustnote/rust-trustnote/releases/download/0.3.0/ubuntu_ttt.zip

2. windows

Https://github.com/trustnote/rust-trustnote/releases/download/0.3.0/windows_ttt.zip


### Experience:


> Take the ubuntu system as an example

### Obtain

Download

```
Wget https://github.com/trustnote/rust-trustnote/releases/download/0.3.0/ubuntu_ttt.zip
```

2. Unzip:

```
Unzip ubuntu_ttt.zip
```

3. Change its permissions to executable:

```
Chmod +x ttt
```

### Configuration

1. In the same directory as ttt, create a new file called settings.json and enter the following information:

```json
{
  "hub_url": [
    "dev.trustnote.org:6616"
  ],
  "mnemonic": "select initial pet jazz alone stamp copper vault private slight rocket stock"
}
```

2. Replace the memory word

You can put your word of help at mnemonic.

The rest will not be changed.

After configuring mnemonic, you can use the info parameter to query the address and balance of the wallet.

### View information

```
./ttt info
```

Get similar information:

```
Current wallet info:

Device_address: 0IKB7F3DAVIB3YHKJYWWVSBC6CSK76IE7
Wallet_public_key: xpub6D9Xmp2Y9XTpZYZ5xk4cNxSQoBufvQ5SWLATBwyaSh38G6aiCrUzUGuEtMoRMPy3a3wKJ8B6obtpUvu89sBbadqah9iXLWohTZi9FWj7JML
└──wallet_id(0): UYwIQm+PIzvY5lceD6uX+yAc86LfaC3RFobSdxGfHmk=
   └──address(0/0): HU475BN5CEEPYL3WPLK5KA3FKXXN5NAD
      ├── path: /m/44'/0'/0'/0/0
      ├── pubkey: A3OTtemVlcteNZafJyXoCbE0UJ5SL74UI0cIjyJC4bCe
      └── balance: 299.999MN

```

The address is followed by the address of the wallet.

The default wallet has no money, so you can open the http://dev.trustnote.org/getTTT input wallet address to receive the test TTT.

After you have received the coins, please check again:

```
./ttt info
```

Usually 3-5 seconds, sometimes 1-2 minutes (depending on network conditions) will have results.

### Transfer

You can go to http://developers.trustnote.org/fancy-address/index.html to generate some test addresses for transferring funds.

I used the production OKLGMIWBCFITVWKZF3JASA23OMZLICSH address as the test address for the transfer.

```
./ttt send -p OKLGMIWBCFITVWKZF3JASA23OMZLICSH 9.99 -t hello
```

Returns the following data:

```
Refresh history done

FROM : HU475BN5CEEPYL3WPLK5KA3FKXXN5NAD
TO :
      Address : OKLGMIWBCFITVWKZF3JASA23OMZLICSH, amount : 9.99
UNIT : ly1DYqhjP/QngSCHP6t1NqumabOZQdR5bSiqzDDt7bc=
TEXT : hello
DATE : 2018-08-15 15:59:27.973
```

The parameter -t hello is a comment message that is chained at the time of transfer. Of course, you can also remove it. which is:

```
./ttt send -p OKLGMIWBCFITVWKZF3JASA23OMZLICSH 9.99
```

### What can I do with the rust version of the command line wallet?

The rust version of the wallet can be placed on the server, and the rust command line wallet can be invoked through other scripts such as php, python, ruby, nodejs, etc., to create a web-based multi-account online wallet.
