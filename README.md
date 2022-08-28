# MoonKitties Interface-Contracts
Various tools and interfaces for community developers.

## IKittyContract.sol -> ERC-721
Interact & get data about from the contract that holds the state of all MoonKitties.

Address: 0xdDF3303084DcB3f77DC36461D0081883e18cF3e0
### Info
- totalSupply() public view returns (uint256);

- getKitty(uint256 _id) external view returns (uint256 genes, uint256 birthTime, uint256 mumId, uint256 dadId, uint256 generation, uint256 id, string memory nickname, bool isRented, uint256 rentingPrice);

- ownerOf(uint256 _tokenId) external view returns (address);

- ownerHasDeattachedItem(address addr, uint256 gType, uint256 gId, uint256 gIndex) external view returns (bool);


- getRevShareKittyOwners() external view returns (address[] memory);  **//Gen 0 Holders**

- isApprovedForAll(address owner, address operator) external view returns (bool);

### Interaction
- setApprovalForAll(address operator, bool approved) external;

- transferFrom(address _from, address _to, uint256 _tokenId) external;

- transferItemFrom(address _from, address _to, uint256 _gearType, uint256 _gearIndex) external;
