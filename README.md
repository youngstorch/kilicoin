Kilicoin integration/staging tree
================================



Copyright (c) 2009-2014 Bitcoin Developers

Copyright (c) 2011-2014 Litecoin Developers

Copyright (c) 2017 - Kilicoin Developers (Developed By : Elia Minja)

What is Kilicoin?
----------------

Kilicoin is a lite version of Bitcoin using scrypt as a proof-of-work algorithm.
 - 1 minute block targets
 - subsidy halves in ~1.22m blocks (~7 years)
 - ~200 million (2 * 10^8) total coins
 - 10000 coins per block
 - 2400 blocks to retarget difficulty

For more information, as well as an immediately useable, binary version of
the Kilicoin client sofware, see 

License
-------

Kilicoin is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Kilicoin
development team members simply pulls it.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/bitcoin/bitcoin/tags) are created
regularly to indicate new official, stable release versions of Kilicoin.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./kilicoin-qt_test

Compiling under different operating systems
-------------------------------------------

### Debian/Ubuntu

    apt-get install build-essential
        libboost-dev libboost-system-dev libboost-filesystem-dev libboost-system-dev \
        libboost-program-options-dev libboost-thread-dev \
        libssl-dev libdb++-dev libdb-dev
    make -f makefile.unix USE_UPNP=-

### Windows

* http://devtome.com/doku.php?id=scrypt_altcoin_cloning_guide#windows_-qt
* https://bitcointalk.org/index.php?topic=149479.0

Dependencies can be found in (dropbox)[https://www.dropbox.com/sh/7f3v6sw6gccno47/AADHQxy5ZHcd7fNjwWvZEjzta]

