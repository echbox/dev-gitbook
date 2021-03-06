# CreditAccount

Implements credit account logic:&#x20;

* Keeps token balances&#x20;
* Stores general parameters: borrowed amount, cumulative index at open and block when it was initialized&#x20;
* Approve tokens for swap/farming contracts&#x20;
* Transfers assets
* Execute valid financial orders

## Code

[CreditAccount.sol](https://github.com/Gearbox-protocol/gearbox-contracts/blob/master/contracts/credit/CreditAccount.sol)

##  State-Changing Functions

### initialize

```
function initialize(address _creditManager) external
```

 Initializes virtual account and connects it with credit manager. Restricted to account factory only

### setGenericParameters

```
function setGenericParameters(
    uint256 _borrowedAmount,
    uint256 _cumulativeIndexAtOpen
) external
```

 Set generic parameters. Restricted to current credit manager only

### updateBorrowedAmount

```
function updateBorrowedAmount(uint256 _borrowedAmount)
    external
```

Updates borrowed amount. Restricted for current credit manager only

### approveTokenFor

```
function approveToken(address token, address swapContract)
    external;
```

Approves token for 3rd party contract. Restricted for current credit manager only

### transfer

```
function transfer(
    address token,
    address to,
    uint256 amount
) external
```

 Transfers tokens from virtual account to provided address. Restricted for pool calls only

### execute

```
function execute(address destination, bytes memory data)
    external
```

Executes financial order on 3rd party service. Restricted for current credit manager only

## Getters

### creditManager

```
function creditManager() external returns (address)
```

Returns address of current credit manager

### borrowedAmount

```
function borrowedAmount() external returns (uint256)
```

Returns amount borrowed to this account

### cumulativeIndexAtOpen

```
function cumulativeIndexAtOpen() external returns (uint256)
```

Cumulative index at credit account opening

### since

```
function since() external returns (address)
```

Returns block number when it was initialised last time



