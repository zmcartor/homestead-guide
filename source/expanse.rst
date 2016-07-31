********************************************************************************
Expanse
********************************************************************************

What is expanse?
================================================================================

Expanse is the name of the currency used within Expanse. It is used to pay for
computation within the EVM. This is done indirectly by purchasing gas for expanse as explained in _`gas`.

Denominations
--------------------------------------------------------

Expanse has a metric system of denominations used as units of Expanse. Each denomination has its own unique name (some bear the family name of seminal figures playing a role in evolution of computer science and cryptoeconomics). The smallest denomination aka *base unit* of Expanse is called Wei. Below is a list of the named denominations and
their value in Wei. Following a common (although somewhat ambiguous) pattern, Expanse also designates a unit (of 1e18 or one quintillion Wei) of the currency. Note that the currency is not called Expanse as many mistakenly think, nor is Expanse a unit.


+-------------------------+-----------+-------------------------------------------+
| Unit                    | Wei Value | Wei                                       |
+=========================+===========+===========================================+
| **wei**                 | 1 wei     | 1                                         |
+-------------------------+-----------+-------------------------------------------+
| **Kwei (babbage)**      | 1e3 wei   | 1,000                                     |
+-------------------------+-----------+-------------------------------------------+
| **Mwei (lovelace)**     | 1e6 wei   | 1,000,000                                 |
+-------------------------+-----------+-------------------------------------------+
| **Gwei (shannon)**      | 1e9 wei   | 1,000,000,000                             |
+-------------------------+-----------+-------------------------------------------+
| **microether (szabo)**  | 1e12 wei  | 1,000,000,000,000                         |
+-------------------------+-----------+-------------------------------------------+
| **milliether (finney)** | 1e15 wei  | 1,000,000,000,000,000                     |
+-------------------------+-----------+-------------------------------------------+
| **expanse**               | 1e18 wei  | 1,000,000,000,000,000,000                 |
+-------------------------+-----------+-------------------------------------------+


Expanse supply
=========================

The total supply of EXP is 11.11m+(numOfBlocksMined*8).
The current number in circulation is only 1m+(numOfBlocksMined*8).

10m is currently being stored in cold storage until the EXP DAO is completed then they will be moved into a democratically controlled organization .


Getting expanse
================================================================================

In order to obtain Expanse, you need to either

* become an Expanse miner (see _`Mining`)  or
* trade other currencies for Expanse using centralized or trustless services

List of centralized exchange marketplaces
--------------------------------------------------------------------------------

========================== ============================
Exchange                   Currencies
========================== ============================
Poloniex                   BTC
Bittrex                    BTC
Bluetrade                  BTC, LTC, DOGE
========================== ============================


Centralized fixed rate exchanges
-----------------------------------


========================== ============================
Exchange                   Currencies
========================== ============================
`Changelly`_              BTC, LTC, DOGE, Other
========================== ============================

.. _Changelly: changelly.com


Trading and price analytics
--------------------------------------------------------------------------------

* `EXP markets exhaustive listing by volume on coinmarketcap <https://coinmarketcap.com/currencies/expanse/#markets>`_
* Aggregating realtime stats of major ETH markets:

  * `EthereumWisdom - Expanse <http://ethereumwisdom.com/#!/expanse>`_
  * `Coinmarketcap <https://coinmarketcap.com/currencies/expanse/>`_


.. _online-wallets-and-storage-solutions:

Online wallets, paper wallets, and cold storage
================================================================================

.. todo::
  This is here just a dumping ground of links and notes
  Please move this over in a listing form to ecosystem

  Keep examples here, maybe explain paranoid practices, list dangers

* Mist Expanse Wallet
    * `Releases to download <https://github.com/expanse-org/mist/releases>`_
* ExpanseWallet
    * `Etherwall source <https://github.com/nrpatten/ExpanseWallet/blob/master/v1.0.0/ExpanseWallet_Installet.exe>`_
* Cold storage
    * `Icebox <https://github.com/ConsenSys/icebox>`_ by `ConsenSys <https://consensys.net/>`_ - Cold storage based on lightwallet with HD wallet library integrated.
    * `Reddit discussion 1 <https://www.reddit.com/r/ethereum/comments/45uvmy/offline_cold_storage_question/offline_cold_storage_question>`_
    * `How to setup a cold storage wallet <https://www.reddit.com/r/ethereum/comments/48wfbv/eli5_how_to_setup_a_cold_storage_wallet_as/>`_

Sending expanse
================================================================================

The `Expanse Wallet  <https://github.com/expanse-org/mist/releases>`_  supports sending expanse via a graphical interface.

Expanse can also be transferred using the **gexp console**.

.. code-block:: console

    > var sender = exp.accounts[0];
    > var receiver = exp.accounts[1];
    > var amount = web3.toWei(0.01, "expanse")
    > exp.sendTransaction({from:sender, to:receiver, value: amount})

For more information of Expanse transfer transactions, see :ref:`account-types-gas-and-transactions`.

Expanse is unique in the realm of cryptocurrencies in that expanse has utility value as a cryptofuel, commonly referred to as "gas". Beyond transaction fees, gas is a central part of every network request and requires the sender to pay for the computing resources consumed. The gas cost is dynamically calculated, based on the volume and complexity of the request and multiplied by the current gas price. Its value as a cryptofuel has the effect of increasing the stability and long-term  demand for expanse and Expanse as a whole. For more information, see :ref:`account-types-gas-and-transactions`.

Gas and expanse
=============================

* https://www.reddit.com/r/ethereum/comments/271qdz/can_someone_explain_the_concept_of_gas_in_ethereum/
* https://www.reddit.com/r/ethereum/comments/3fnpr1/can_someone_possibly_explain_the_concept_of/
* https://www.reddit.com/r/ethereum/comments/49gol3/can_ether_be_used_as_a_currency_eli5_ether_gas/


Gas is supposed to be the constant cost of network resources/utilization. You want the real cost of sending a transaction to always be the same, so you can't really expect Gas to be issued, currencies in general are volatile.

So instead, we issue Expanse whose value is supposed to vary, but also implement a Gas Price in terms of Expanse. If the price of Expanse goes up, the Gas Price in terms of Expanse should go down to keep the real cost of Gas the same.

Gas has multiple associated terms with it: Gas Prices, Gas Cost, Gas Limit, and Gas Fees. The principle behind Gas is to have a stable value for how much a transaction or computation costs on the Expanse network.

* Gas Cost is a static value for how much a computation costs in terms of Gas, and the intent is that the real value of the Gas never changes, so this cost should always stay stable over time.
* Gas Price is how much Gas costs in terms of another currency or token like Expanse. To stabilize the value of gas, the Gas Price is a floating value such that if the cost of tokens or currency fluctuates, the Gas Price changes to keep the same real value. The Gas Price is set by the equilibrium price of how much users are willing to spend, and how much processing nodes are willing to accept.
* Gas Limit is the maximum amount of Gas that can be used per block, it is considered the maximum computational load, transaction volume, or block size of a block, and miners can slowly change this value over time.
* Gas Fee is effectively the amount of Gas needed to be paid to run a particular transaction or program (called a contract). The Gas Fees of a block can be used to imply the computational load, transaction volume, or size of a block. The gas fees are paid to the miners (or bonded contractors in PoS).
