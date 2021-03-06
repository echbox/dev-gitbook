# ACL

ACL keeps permission for different addresses. For the moment, it keeps 2 different roles:

### [PausableAdmin](../../security/anomaly-detection.md#pausable-admin-role-and-pausable-trait)&#x20;

Can pause and unpause contracts

### Configurator

Can configure contracts parameters

## Code

[ACL.sol](https://github.com/Gearbox-protocol/gearbox-contracts/blob/master/contracts/core/ACL.sol)

## State-Changing Functions

### addPausableAdmin

```
function addPausableAdmin(address newPausableAdminAddress)
external
```

Adds pausable admin address to the list

## Getters

### getPausableAdminById

```
function getPausableAdminById(uint256 id) 
external 
view 
returns (address)
```

 Returns pausable admin address by id

### getPausableAdminsCount

```
function getPausableAdminsCount() 
external 
view 
returns (uint256)
```

 Counts pausable admins

### isPausableAdmin

```
function isPausableAdmin(address addr) 
external 
view 
returns (bool)
```

 Returns true if the address is pausable admin and false if not

### isConfigurator

```
function isConfigurator(address addr) 
external view returns (bool)
```

 Returns true if addr has configurator rights
