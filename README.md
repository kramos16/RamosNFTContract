# RamosNFTContract
This contract serves as a basic foundation for managing NFTs, providing essential functionalities for minting, listing, and retrieving NFT metadata. 
## Description
Users can adapt and expand upon this code to create more complex NFT-related applications, such as digital art galleries or virtual item collections.
### Executing program
pragma solidity ^0.8.0;

contract RamosNFTContract {
    struct NFT {
        string name;
        string eyeColor;
        string shirtType;
        string bling;
    }

    NFT[] public nftCollection;

    function mintNFT(
        string memory name,
        string memory eyeColor,
        string memory shirtType,
        string memory bling
    ) public {
        NFT memory nft = NFT(name, eyeColor, shirtType, bling);
        nftCollection.push(nft);
    }

    function listNFTs() public view returns (NFT[] memory) {
        return nftCollection;
    }

    function getTotalSupply() public view returns (uint256) {
        return nftCollection.length;
    }
}
## License
This project is licensed under the MIT License - see the LICENSE.md file for details
