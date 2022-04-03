# gdsc-blockchain-task



// SPDX-License-Identifier: UNLICENSED
pragma solidity >=0.7.0 <0.9.0;

contract SimpleStorage {
    uint result;
    uint histresult;
    uint i=0;
    uint j=0;
    uint k=0;
    uint l=0;

    function add(uint x, uint y) public 
    {
        result = x + y;
        i++;
    }

    function sub(uint x, uint y) public {
        result = x - y;
        j++;
    }

    function multiply(uint x, uint y) public {
        result = x * y;
        k++;
    }

    function divide(uint x, uint y) public {
        require(y!=0,'Division by zero not possible');
        result = x / y;
        l++;
    }

    function get() public view returns (uint) {
        return result;
    }

    function add_history() public {
        histresult = i;
    }

    function sub_history() public {
        histresult = j;
    }

    function multiply_history() public {
        histresult = k;
    }

    function divide_history() public {
        histresult = l;
    }

    function show_history() public view returns (uint) {
        return histresult;
    }
}
