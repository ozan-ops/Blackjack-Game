# Blackjack Game

## Overview
This Python program simulates a game of Blackjack. The player can bet chips, be dealt cards, and decide whether to hit or stand to get as close to 21 as possible without going over. The game includes functionality for handling bets, adjusting for Aces, and comparing the player's hand against the dealer's hand to determine the winner.

## Game Description
Blackjack is a card game where players try to get a hand value as close to 21 as possible without exceeding it. The dealer also plays and tries to beat the player's hand by having a higher value without going over 21. Face cards (Jack, Queen, King) are worth 10 points, Aces are worth 1 or 11 points, and all other cards are worth their face value.

## Functions

### `Card` Class
- `__init__(self, suit, rank)`: Initializes a card with a suit and rank.
- `__str__(self)`: Returns a string representation of the card.

### `Deck` Class
- `__init__(self)`: Initializes a deck of 52 cards.
- `__str__(self)`: Returns a string representation of the entire deck.
- `shuffle(self)`: Shuffles the deck.
- `deal(self)`: Deals a single card from the deck.

### `Hand` Class
- `__init__(self)`: Initializes a hand with an empty list of cards and a value of 0.
- `add_card(self, card)`: Adds a card to the hand and updates the hand's value.
- `adjust_for_ace(self)`: Adjusts the hand's value if there are Aces and the value exceeds 21.

### `Chips` Class
- `__init__(self)`: Initializes the chips with a total of 100 and a bet of 0.
- `win_bet(self)`: Increases the total by the bet amount.
- `lose_bet(self)`: Decreases the total by the bet amount.

### Other Functions
- `take_bet(chips)`: Prompts the player to input a bet amount and checks if it is valid.
- `hit(deck, hand)`: Deals a card from the deck and adds it to the hand.
- `hit_or_stand(deck, hand)`: Prompts the player to hit or stand.
- `show_some(player, dealer)`: Displays the player's hand and the dealer's hand with one card hidden.
- `show_all(player, dealer)`: Displays all cards in the player's and dealer's hands.
- `player_busts(player, dealer, chips)`: Handles the scenario when the player busts.
- `player_wins(player, dealer, chips)`: Handles the scenario when the player wins.
- `dealer_busts(player, dealer, chips)`: Handles the scenario when the dealer busts.
- `dealer_wins(player, dealer, chips)`: Handles the scenario when the dealer wins.
- `push(player, dealer)`: Handles the scenario when the player and dealer tie.

## Usage
To play the game:
1. Run the script.
2. Enter the bet amount when prompted.
3. Choose to hit or stand when prompted.
4. The game will display the result and prompt if you want to play another round.

## Example
Here's an example interaction with the program:

Welcome to Blackjack!
How many chips would you like to bet? 50

Dealer's Hand:
<card hidden>
Eight of Hearts

Player's Hand:
Two of Clubs
Jack of Diamonds
Would you like to Hit or Stand? Enter 'h' or 's' h

Dealer's Hand:
<card hidden>
Eight of Hearts

Player's Hand:
Two of Clubs
Jack of Diamonds
Three of Spades
Would you like to Hit or Stand? Enter 'h' or 's' s
Player stands. Dealer is playing.

Dealer's Hand:
Eight of Hearts
Six of Diamonds
Three of Clubs

Player's Hand:
Two of Clubs
Jack of Diamonds
Three of Spades

Dealer wins!
Player's winnings stand at 50
Would you like to play another hand? Enter 'y' or 'n'

## Note
- Ensure that the inputs for the bet amount and hit/stand choice are valid.
- The game continues until the player decides to stop playing.

Enjoy the game of Blackjack!
