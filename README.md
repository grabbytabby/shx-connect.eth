# shx-connect.eth
shx-connect.com migration Phase I

git clone https://shx-connect.eth.squarespace.com/template.git


protocol: shxmnp
port: rule 2407

host/server: dev.squarespace.com
remote path (initial feedler): /shx-connect.eth-shx-connect.com/

username: your account email address
password: your account password


Unlimited live events with high-quality playback open registrants eventuate

     Browser-based production tools with costume blue/green screngem-media, 
     scenes, layouts, and automated podcerts
    Custom guest speaker interface (livinrume guest speakers)
     Eventuate and viewer-level analyratix
    Volohgrm-on-demand handings(hosting) with book,pages,chapters, 
    writeforms, and migradabeddable CTAs
tantellyzer(Writer) publisher Ascap/Bmi_Deroylety-Deroy musicweb3wallet powered by SHX-Connect erc20 token
      
     
#
# Connector_Generic_Conn_02x06_Odd_Even
#
DEF Connector_Generic_Conn_02x06_Odd_Even J 0 40 Y N 1 F N
F0 "J" 50 300 50 H V C CNN
F1 "Connector_Generic_Conn_02x06_Odd_Even" 50 -400 50 H V C CNN
F2 "" 0 0 50 H I C CNN
F3 "" 0 0 50 H I C CNN
$FPLIST
 Connector*:*_2x??_*
$ENDFPLIST


// SPDX-License-Identifier: GPL-3.0
pragma solidity ^0.8.4;

contract Coin {
    // The keyword "public" makes variables
    // accessible from other contracts
    address public minter;
    mapping (address => uint) public balances;

    // Events allow clients to react to specific
    // contract changes you declare
    event Sent(address from, address to, uint amount);

    // Constructor code is only run when the contract
    // is created
    constructor() {
        minter = msg.sender;
    }

    // Sends an amount of newly created coins to an address
    // Can only be called by the contract creator
    function mint(address receiver, uint amount) public {
        require(msg.sender == minter);
        balances[receiver] += amount;
    }

    // Errors allow you to provide information about
    // why an operation failed. They are returned
    // to the caller of the function.
    error InsufficientBalance(uint requested, uint available);

    // Sends an amount of existing coins
    // from any caller to an address
    function send(address receiver, uint amount) public {
        if (amount > balances[msg.sender])
            revert InsufficientBalance({
                requested: amount,
                available: balances[msg.sender]
            });

        balances[msg.sender] -= amount;
        balances[receiver] += amount;
        emit Sent(msg.sender, receiver, amount);
    }
}
Deroy a defy-protocol
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.16 <0.9.0;

contract SimpleStorage {
    uint storedData;

    function set(uint x) public {
        storedData = x;
    }

    function get() public view returns (uint) {
        return storedData;
    }
}
