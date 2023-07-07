**Error Handling**
This Solidity program is an error-handling program that demonstrates the use of require, revert, and assert statements. 

**Description**
Solidity has three error-handling methods: 
* require(): which validates conditions before function execution.
* assert(): The assert function, like require, is a convenience function that checks for conditions.
            If a condition fails, then the function execution is terminated.
* revert(): causes the EVM to revert all the changes made to the state, and things return to the initial state or the state before the function call was made.


**Getting Started
Executing program**
pragma solidity ^0.8.0;

contract ExceptionHandling {
    function requireexample(uint256 x) public pure returns (uint256) {
        // The require statement is used to validate conditions and revert if the condition is not met.
        require(x > 0, "Value must be greater than zero");
        return x;
    }
    
    function assertExample(uint256 x) public pure returns (uint256) {
        // The assert statement is used to check for internal errors and revert if the condition is not met.
        assert(x > 0);
        return x;
    }
    
    function revertExample(uint256 x) public pure returns (uint256) {
        // The revert statement is used to revert the transaction and provide a custom error message.
        if (x == 0) {
            revert("Value must not be zero");
        }
        return x;
    }
}
Compile the code using Solidity Compiler, set to "0.8.4", 
click "Compile errorhandling.sol" button. 
Deploy the contract by selecting "errorhandling" from the dropdown menu and clicking "Deploy" button.

**Author**
Baby Monal

