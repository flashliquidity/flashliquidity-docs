---
description: FlashLiquidity flash loans
---

# Flash Loans

![](../.gitbook/assets/flashloan.jpg)

{% hint style="success" %}
Flash Loans allow you to borrow any available amount of assets without putting up any collateral, as long as the liquidity is returned to the protocol within one block transaction.
{% endhint %}

* Flash swaps farms contracts can lend out up to the entire rewards token balance in flash loan operations.
* flashLoan() function allows borrower to access liquidity of flash swaps farms reward token balance.
* 0.05% fees. (Generates yield for the arbitrage profits deposited into farms)
* NOTE: _flash loan fee_ is waived for approved addresses (zero fee flash loans)
* After some sanity checks, the Farm transfers the requested amounts of the reward token balance to your contract, then calls onFlashLoan() on receiver contract.

```
interface IFlashBorrower {
    /// @notice The flashloan callback. `amount` + `fee` needs to repayed to msg.sender before this call returns.
    /// @param sender The address of the invoker of this flashloan.
    /// @param token The address of the token that is loaned.
    /// @param amount of the `token` that is loaned.
    /// @param fee The fee that needs to be paid on top for this loan. Needs to be the same as `token`.
    /// @param data Additional data that was passed to the flashloan function.
    function onFlashLoan(
        address sender,
        address token,
        uint256 amount,
        uint256 fee,
        bytes calldata data
    ) external;
}
```
