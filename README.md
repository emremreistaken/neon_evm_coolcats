"Neon Cats" uses the ERC721 standard for NFTs. Each token minted from this contract represents a unique Cool Cat. This contract is deployed on NeonEVM. The contract address of the 'NeonEVM CoolCats' is 0x15883162dcb574bf049cd0821779124d24d5ea46. You can see the transactions carried out on this contract via NeonScan.

Here's a breakdown of what the contract and its functions do:

Contract Declaration: The contract is named CoolCats and it extends ERC721Enumerable and Ownable. ERC721Enumerable is a variant of the ERC721 standard that adds functionality for enumerating over all of the NFTs owned by a particular address. Ownable is a contract that has an owner address, and provides authorization control functions.

Variables: The contract has several state variables including _baseTokenURI, _reserved, _price, _paused, and four addresses (t1, t2, t3, t4). The _baseTokenURI is used to form the metadata URI for each token. _reserved is the number of tokens reserved for the contract owner. _price is the price for each token in Ether. _paused is a boolean that indicates whether the token sale is paused. The four addresses are presumably the addresses of the team members.

adopt: This function allows a user to "adopt" (or purchase) a number of cats. It checks that the sale is not paused, the number of cats being adopted is less than 21, the total supply after adoption is less than the maximum supply minus the reserved cats, and the correct amount of Ether is sent. It then mints the new cats to the sender.

walletOfOwner: This function returns all token IDs owned by a particular address. It does this by iterating over all tokens owned by the address and adding them to an array.

setPrice: This function allows the contract owner to change the price of the cats. This could be useful if, for example, the price of Ether changes dramatically and the owner wants to keep the price of the cats stable in fiat currency terms.

_baseURI: This is an internal function that overrides the _baseURI function in the ERC721 contract. It returns the base URI for the token metadata.

setBaseURI: This function allows the contract owner to change the base URI for the token metadata.

getPrice: This function returns the current price of the cats.

giveAway: This function allows the contract owner to give away some of the reserved cats. It checks that the amount being given away is less than or equal to the number of reserved cats, then mints the cats to the specified address and decreases the number of reserved cats.

pause: This function allows the contract owner to pause or unpause the sale of cats.

withdrawAll: This function allows the contract owner to withdraw all Ether from the contract, splitting it evenly between the four team member addresses.
