# 

| software name      | license   | support                       |
| ------------------ | --------- | ----------------------------- |
| maidenlane v.1.9.0 | BSD-3 New | <support@freight.zendesk.com> |

Maidenlane v1.9.0 + Documentation last updated: 5/16/2020

  - :  
    danger

v2.0.0 will be incompatible with any version below 2.0.0 + Support for
below version 2.0.0 will be on-going through 2022.

  - :  
    \= UniversalABI

**UniversalABI**

# setTarget - read

|name |type |description |----|----|-------- ||bytes4| ||address| **Add
Documentation for the method here**

# getController - view

*No parameters* **Add Documentation for the method here**

# getTarget - view

|name |type |description |----|----|-------- ||bytes4| **Add
Documentation for the method here**

# changeController - read

|name |type |description |----|----|-------- ||address| **Add
Documentation for the method here**

# getMaster - view

*No parameters* **Add Documentation for the method here**

# pause - read

*No parameters* **Add Documentation for the method here**

# changeMaster - read

|name |type |description |----|----|-------- ||address| **Add
Documentation for the method here**

# setTarget - read

|name |type |description |----|----|-------- |functionSel|bytes4|The
function selector for which routing is adjusted |newTarget|address|The
new destination to which calls with the selector will be routed Allows
the controller to set a delegate target for a function selector Returns:
*No parameters*

# setMaster - read

|name |type |description |----|----|-------- |newMaster|address|The new
default delegate target for the universal proxy Allows the controller to
set a new master address. Note that *this contract* is deployed at the
master address by default. Returns: *No parameters*

# getController - view

*No parameters* Returns the controller address of the universal proxy
that is calling this contract. Return : The controller address of the
universal proxy Returns: |name |type |description |----|----|--------
||address|

# getTarget - view

|name |type |description |----|----|-------- |functionSel|bytes4|The
function selector to check Returns the address to which execution is
delegated for a given function selector Return : address The address to
which execution will be delegated for the selector Returns: |name |type
|description |----|----|-------- ||address|

# changeController - read

|name |type |description |----|----|-------- |newController|address|The
address to which permissions will be transferred Allows the controller
to transfer permissions to a new address Returns: *No parameters*

# getMaster - view

*No parameters* Returns the master address of the universal proxy that
is calling this contract. Return : The master address of the universal
proxy Returns: |name |type |description |----|----|-------- ||address|

# pause - read

*No parameters* Allows the controller to flip the pause status of the
application Returns: *No parameters*

# fallback - read

*No parameters* **Add Documentation for the method here** Returns: *No
parameters*

# onERC721Received - read

|name |type |description |----|----|-------- |\_operator|address|The
address which called `safeTransferFrom` function |\_from|address|The
address which previously owned the token |\_tokenId|uint256|The NFT
identifier which is being transferred |\_data|bytes|Additional data with
no specified format The ERC721 smart contract calls this function on the
recipient after a `transfer`. This function MAY throw to revert and
reject the transfer. Return of other than the magic value MUST result in
the transaction being reverted. Note: the contract address is always the
message sender. Return :
`bytes4(keccak256("onERC721Received(address,address,uint256,bytes)"))`
unless throwing Returns: |name |type |description |----|----|--------
||bytes4|

Module NFTExtennded

# supportsInterface - view

|name |type |description |----|----|-------- |\_id|bytes4| **Add
Documentation for the method here** Returns: |name |type |description
|----|----|-------- ||bool|

# name - view

*No parameters* **Add Documentation for the method here** Returns: |name
|type |description |----|----|-------- ||string|

# getApproved - view

|name |type |description |----|----|-------- |\_tokenId|uint256|The
token being queried Get the approved address of the specified token
Return : The approved address of the specified token Returns: |name
|type |description |----|----|-------- ||address|

# approve - read

|name |type |description |----|----|-------- |*approved|address|
|\_tokenId|uint256| **Add Documentation for the method here** Returns:
\_No parameters*

# totalSupply - view

*No parameters* **Add Documentation for the method here** Returns: |name
|type |description |----|----|-------- ||uint256|

# signedTransfer - read

|name |type |description |----|----|-------- |*from|address|The address
that should own NFT at the start of the transaction |\_to|address|The
recipient of the transfer |\_tokenId|uint256|The id of the token to be
transferred |\_sig|bytes|The signature that may authorize the transfer
Transfers an NFT token if the message representing the transaction was
signed by \_from Returns: \_No parameters*

# createRecord - read

|name |type |description |----|----|-------- |*record|bytes32|
|\_participant|address| |\_sOwner|bytes| |\_sPart|bytes| **Add
Documentation for the method here** Returns: \_No parameters*

# transferFrom - read

|name |type |description |----|----|-------- |*from|address|
|\_to|address| |\_tokenId|uint256| **Add Documentation for the method
here** Returns: \_No parameters*

# tokenOfOwnerByIndex - view

|name |type |description |----|----|-------- |\_owner|address|An address
where we are interested in NFTs owned by them |\_index|uint256|A counter
less than `balanceOf(_owner)` Throws if `_index` \>= `balanceOf(_owner)`
or if `_owner` is the zero address, representing invalid NFTs. Return :
The token identifier for the `_index`th NFT assigned to `_owner`, (sort
order not specified) Returns: |name |type |description
|----|----|-------- ||uint256|

# safeTransferFrom - read

|name |type |description |----|----|-------- |*from|address|
|\_to|address| |\_tokenId|uint256| **Add Documentation for the method
here** Returns: \_No parameters*

# tokenByIndex - view

|name |type |description |----|----|-------- |\_index|uint256|A counter
less than `totalSupply()` Throws if `_index` \>= `totalSupply()`. Return
: The token identifier for the `_index`th NFT, (sort order not
specified) Returns: |name |type |description |----|----|--------
||uint256|

# versionRecordSigned - read

|name |type |description |----|----|-------- |*record|bytes32|
|\_updated|bytes32| |\_sig|bytes| **Add Documentation for the method
here** Returns: \_No parameters*

# ownerOf - view

|name |type |description |----|----|-------- |\_tokenId|uint256|The id
of the specified nft token Returns the owner address of the specified
token Return : The address of the owner of the token Returns: |name
|type |description |----|----|-------- ||address|

# balanceOf - view

|name |type |description |----|----|-------- |\_owner|address|The owner
of the nfts Count all of the nfts owned by the \_owner Return : Returns
a count of the nfts owned by the \_owner Returns: |name |type
|description |----|----|-------- ||uint256|

# versionRecord - read

|name |type |description |----|----|-------- |*record|bytes32|
|\_updated|bytes32| **Add Documentation for the method here** Returns:
\_No parameters*

# symbol - view

*No parameters* **Add Documentation for the method here** Returns: |name
|type |description |----|----|-------- ||string|

# setApprovalForAll - read

|name |type |description |----|----|-------- |*operator|address|
|\_approved|bool| **Add Documentation for the method here** Returns:
\_No parameters*

# safeTransferFrom - read

|name |type |description |----|----|-------- |*from|address|
|\_to|address| |\_tokenId|uint256| |\_data|bytes| **Add Documentation
for the method here** Returns: \_No parameters*

# isApprovedForAll - view

|name |type |description |----|----|-------- |\_owner|address|The
address that owns the NFTs |\_operator|address|The address that acts on
behalf of the owner Return : True if `_operator` is an approved operator
for `_owner`, false otherwise Returns: |name |type |description
|----|----|-------- ||bool|

# RecordCreated - read

|name |type |description |----|----|-------- |locator|uint256|
|owner|address| |participant|address| **Add Documentation for the method
here** Returns: *No parameters*

# RecordUpdated - read

|name |type |description |----|----|-------- |record|uint256|
|updated|uint256| |owner|address| **Add Documentation for the method
here** Returns: *No parameters*

# Approval - read

|name |type |description |----|----|-------- |*owner|address|
|\_approved|address| |\_tokenId|uint256| **Add Documentation for the
method here** Returns: \_No parameters*

# Transfer - read

|name |type |description |----|----|-------- |*from|address|The address
that should own NFT at the start of the transaction |\_to|address|The
recipient of the transfer |\_tokenId|uint256|The id of the token to be
transferred Transfers an NFT token if the message representing the
transaction was signed by \_from Returns: \_No parameters*

# ApprovalForAll - read

|name |type |description |----|----|-------- |*owner|address|
|\_operator|address| |\_approved|bool| **Add Documentation for the
method here** Returns: \_No parameters*
