# ShoppingMall Smart Contract

This is a Solidity smart contract for a simple shopping mall application where users can purchase items from three different floors and take advantage of a special offer.

## Features

1. **Purchases Tracking**: Keeps track of the number of items purchased from three different floors for each user.
2. **Buy Items Functionality**: Allows users to buy items from each floor with certain restrictions.
3. **Buy 2 Get 1 Offer**: A special offer function to check if the purchased items are eligible for a "buy 2 get 1 free" offer.

## Contract Details

### Purchase Structure

The `Purchase` struct is used to store the number of items bought from each floor for each user.

### State Variables

- `purchases`: A mapping that stores the `Purchase` struct for each user address.

### Functions

#### `buyItems`

This function allows users to buy items from the three floors. It takes the following parameters:
- `floor1Items`: The number of items to buy from floor 1.
- `floor2Items`: The number of items to buy from floor 2.
- `floor3Items`: The number of items to buy from floor 3.

Restrictions:
- Users must buy more than 1 item from each floor.
- Users cannot buy more than 5 items from any single floor in one transaction.

If these conditions are met, the purchased items are added to the user's total purchases for each floor.

#### `buy2Get1`

This function checks if the number of items is eligible for a "buy 2 get 1 free" offer. It takes the following parameter:
- `itemCount`: The number of items being checked.

Restriction:
- The offer is only applicable if the item count is an even number.

If the item count is not a multiple of 2, the function will revert with an error message.

## Usage

1. Deploy the contract to a compatible Ethereum network.
2. Users can call the `buyItems` function to purchase items from the mall's floors, adhering to the specified restrictions.
3. Users can call the `buy2Get1` function to check if their item count qualifies for the "buy 2 get 1 free" offer.

This contract is designed to be a simple example of how to manage purchases and offers in a shopping mall context using Solidity.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Author

Abhishek 

abhishek7abhi7799@gmail.com
