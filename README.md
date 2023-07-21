# ECEGameDOS
Code for a game of DOS (version of UNO)
Specifications
1. DOS cards are represented as variables of the following type:
typedef struct card_s { 
char color[10]; 
int value;
char action[15];
struct card_s *pt;
} card;
You are allowed to add attributes to this definition, but not to remove any. The action field is used to 
denote the function of action cards.
2. The draw pile is implemented by an array of 108 cards. You may also implement the deck as a linked
list.
3. Each player’s hand is implemented using a linked list of cards. The list is initially populated with 
the cards dealt to each player. A card drawn (or played) by each player is added to (or deleted from) 
the respective list.
4. The center row is implemented as a linked list.
5. A sample input file is provided for loading the card deck. This will be used in testing, so ensure you can load 
cards from this file.


Setup
1. The following action cards are included:
• #: It represents any number from 1-10 of the specific color.
• Multi-color 2: It represents a two of any color.
2. Deal seven (7) cards to each player. Starting with player 1, play proceeds according to the rules.

   
GamePlay
The gameplay process is described at https://www.unorules.com/dos-rules/. Some game 
simplifications are as follows.
• At the beginning of the game, the user can choose to shuffle the deck or load a predefined sequence of 
cards from a file (for testing).
• There is no need to keep track of the discard pile. If the game has not ended by the time the draw pile 
is exhausted, the game terminates, and the winner is the one with the lowest point total in hand.
• Limit the game to two players.
• Limit the game to one round of play. Once one person goes out, they are the winner. Report out their 
score

Sample Execution
Let’s Play a Game of DOS
Press 1 to shuffle the DOS deck or 2 to load a deck from a file: 1 
The deck is shuffled. Press any key to deal cards
Player’s one hand: 6 red, 5 green, 2 anycolor, 10 blue, # green, 4 yellow, 1 red
Centerline 5 green, 8 yellow
How many cards do you want to play on 5 green: 1 
Select a card from 1-7: 2
Player’s one hand: 6 red, 2 anycolor, 10 blue, # green, 4 yellow, 1 red 
How many cards do you want to play on 8 yellow: 2
Select cards from 1-6: 1,3
4
That selection does not total to the center row card. Select again.
Player’s one hand: 6 red, 2 anycolor, 10 blue, # green, 4 yellow, 1 red 
How many cards do you want to play on 8 yellow: 2
Select two cards from 1-6: 1,2
There are no more center row cards to match.
You color matched and get to play 1 card(s) on the center row.
Player’s one hand: 10 blue, # green, 4 yellow, 1 red 
Select one additional card from 1-4 to place to the center row: 3 
Player’s one hand: 10 blue, # green, 1 red
Player’s two turn.
Player’s two hand: 8 blue, 4 green, 7 green, 3 green, 1 yellow, 2 anycolor, 1 blue
Centerline 4 yellow, 10 green, 3 blue
How many cards do you want to play on 4 yellow: 1
Select a card from 1-7: 2
Player’s two hand: 8 blue, 7 green, 3 green, 1 yellow, 2 anycolor, 1 blue
How many cards do you want to play on 10 green: 2
Select two cards 1-6: 2,3
Player’s two hand: 8 blue, 1 yellow, 2 anycolor, 1 blue
How many cards do you want to play on 3 blue: 2
Select two cards 1-4: 3,4
Player’s two hand: 8 blue, 1 yellow
There are no more center row cards to match.
You color matched and get to play 2 card(s) on the center row.
Player’s two hand: 8 blue, 1 yellow
Select 2 additional card(s) from 1-2 to place to the center row: 1,2 
Dealing 2 additional card(s) to other players.
Player’s two hand: 
Player two wins with 62 points!
