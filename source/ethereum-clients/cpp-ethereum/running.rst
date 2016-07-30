################################################################################
Running
################################################################################

Running exp without any argument will synchronise your node to the public blockchain.
It is also possible to create or synchronise to another blockchain (see :ref:`custom blockchain using exp <custom-networks-exp>`).

Interacting with your node can be done using either gexp or the expanse console:

**Using gexp**

.. code:: Console

   > gexp attach //attach gexp to a running exp node.

**Using the expanse console**

The expanse console is a node.js application which connect to a running exp/gexp node and provide access to the web3 object.

.. note:: https://github.com/expanse-org/expanse-console

It can be installed using npm:

.. note:: | > npm install -g expanse-console
            | > ethconsole

.. note:: | **Usage:**
        | ethconsole [javascript file] [ipc socket]
        | Connects to an expanse node via ipc in order to control it remotely
        | through global variable web3 (web3.admin is also present).
        | If no arguments are given, connects to the default ipc socket
        | and drops into interactive mode.
        | Arguments:
        | <ipc socket path>  connect to the given ipc socket (use ipc://<path> if it does not end with .ipc)
        | <javascript file>    execute the given javascript file that has to end in .js non-interactively.
        | The script has to call process.exit() in order to terminate the console.
