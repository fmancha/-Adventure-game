# Adventure Game
In this project, you'll make a simpler version of an old-fashioned text-based adventure game.

## Project Overview
This project use the skills of Python and asks you to re-create an old-fashioned text-based adventure game.

In order to build a program like this, we should first completely understand what it does. Take a notepad out, and play the game multiple times. The game will present you some scenarios and ask you to make one of 2 choices, by entering 1 or 2. In your notepad, record what happens each time you make a certain choice.

## Record Scenarios Make One or Two Choices

![](Scenarios-images/Screen%20Shot%202020-09-09%20at%2012.57.46%20PM.png)

![](Scenarios-images/Screen%20Shot%202020-09-09%20at%2012.59.05%20PM.png)

![](Scenarios-images/Screen%20Shot%202020-09-09%20at%2012.59.31%20PM.png)

![](Scenarios-images/Screen%20Shot%202020-09-09%20at%2012.59.52%20PM.png)

![](Scenarios-images/Screen%20Shot%202020-09-09%20at%201.01.02%20PM.png)

![](Scenarios-images/Screen%20Shot%202020-09-09%20at%201.02.10%20PM.png)

![](Scenarios-images/Screen%20Shot%202020-09-09%20at%201.03.21%20PM.png)

![](Scenarios-images/Screen%20Shot%202020-09-09%20at%201.11.40%20PM.png)

![](Scenarios-images/Screen%20Shot%202020-09-09%20at%201.12.32%20PM.png)

## Description 

As you can see, this is only a very short game with a couple of choices available to the player. We did that on purpose, to keep it simple. If we were making a complete game, we would expand it a great deal, and probably give the player a whole world to explore. But for this project, the idea is to focus on some key things that we need if want to make a working game:

The game gives players a description of what's happening, and then asks them to make a choice.
Something different happens depending on the choice the player made.
The game also includes some random factors, so that it's a little different each time.
The game has conditions for winning and losing.
When the game is over, it asks if the player wants to play again.
These are the key features that your project will need to have in order to make it into a playable game. We'll go over each of them in more detail below.

As long as your program does all of the things listed in the instructions below, you are free to be as creative as you like!

## Project Instructions
#### 1. Print descriptions of what's happening for the player
One thing the game will need to do is to print messages for the player to describe what is happening. these lines are printed on **Record Scenarios Make One or Two Choices**
#### 2. Pausing between printing descriptions
* Use **time.sleep** to create a delay between messages. if you like, you can experiment with delays of different lengths for dramatic effect.
* Run your code to check that it still works. (it's a good idean to do this frequently while you work!)
#### 3. Give the player some choices
Up till now, our program prints the introduction of the game, with short pauses in between each sentence. Another important element of any good adventure game is choice. To do this, you'll need to get some input from the player, and then change what happens depending on what that input is.  In the example game, that looked like:

*Enter 1 to knock on the door of the house.*  
*Enter 2 to peer into the cave.*  
*What would you like to do?*  
*(Please enter 1 or 2).*

* Present the player with a choice, and collect their response using the **input** funtion.
* Have something different happend depending on the player's choice.

#### 4. Make sure the player gives a valid input
Up till now, our program prints a description of the game-world to the player, gives them a choice, and prints what happens depending on their choice. An important thing to notice in the example game is that if the player enters something other than **1** or **2**, the game keeps asking them for a **1** or **2**. We don't want the game to accept invalid input, like **75** or **foo!**

If the player tries to respond with something invalid, your program should ask them to try again—and it should keep asking them to try again until they give valid input.
* Add code to check the input to see if it's valid. If they entered an invalid response, it should ask them to try again.

#### 5. Add functions and refactor your code
By now, you may have noticed that some of your code is getting pretty messy, and some parts may be kind of repetitive. If you haven't already, this would be a good time to consider defining some functions, and moving some of your code into those functions.

For example, you probably have a lot of code that looks like this:

**print** *("You find yourself standing in an open field, filled with grass and",*
      *"yellow wildflowers.")*
     
**time.sleep(2)**

**print** *("Rumor has it that a wicked fairie is somewhere around here, and has",*
      *"been terrifying the nearby village.")*
      
**time.sleep(2)**

**print** *("In front of you is a house.")*

**time.sleep(2)**

**print** *("To your right is a dark cave.")*

**time.sleep(2)**

**print** *("In your hand you hold your trusty (but not very effective) dagger.")*

**time.sleep(2)**

*....*

* Add some funtion definitions to your code to help organize it better 

#### 6. Use randomness in your game
Another key feature of most games is randomness or chance. If everything always happens exactly the same way, it can become boring and predictable.

There are all sorts of ways you could use randomness in your game. Here are just a few possibilities:

*In the example game, the enemy creature is selected randomly each time they play.* *Sometimes it's a pirate, sometimes it's a troll, and so on.*

*You could do something similar to randomize which weapons or magical items the* *player encounters.*

*You could include a combat simulation in which the player and enemy deal random* *amounts of damage to one another (you may remember that we did something like this* *earlier in the course).*

All of these can be done using Python's **random** module and the **random.choice** and **random.randint** functions that we learned about earlier. For example: At the start of each game, you can set the random enemy creature.

There are countless other possible ways to use randomness in your game—feel free to be creative here.

* Add randomness to your game, so that the player sees something different each time they play.
* Test your code with different scenarios. Check for any errors that happend.

#### 7. Create win and lose conditions
Eventually, the game should come to an end—and tell the player that they won or lost.

The end result of the game should be influenced by the player's choices (and possibly some degree of randomness as well). Generally, it's a good idea to use randomness to only partially influence the outcome. If what happens to the player is completely random, the player will feel out of control and probably won't enjoy it.

For example, in our example game, the player fights the enemy creature. If they win the fight, they win the game!
* Create conditions to end the game, and tell the player that they won or lost.

#### 8. Check if the player wants to play again
When Python gets to the end of your script, it will exit back to the terminal. But that's not a good player experience. Instead, it would be better if the game asked the player whether they want to play again:

*GAME OVER*

*Would you like to play again? (y/n)*

Just like with other choices you've asked the player to make, this will need to get the player's input and then check if the input is valid.

If the player indicates that yes, they want to play again, then the game should start over. Depending on what you added to your game, there may be some things that need to be reset. For example, if your player has a health score or they picked up magical items, these should go back to the way they were when the game starts over.

For example, in our example game, after the player fights the enemy, they are asked if they want to play the game again irrespective of whether or not they won.

* Add code to your program so that it checks wheter the player wants to play again.
* If the player say they do want to play again, the game should start over form the beginning with the original setting.

#### 9. Check your style with pycodestyle
When you're all done with your program, be sure to check it using the **pycodestyle** tool—and then fix any issues it raises.

*pycodestyle adventure_game.py*

* Run **pycodestyle** on your game and fix all the issues it raises.

#### 10. Test Your Code
* The game plays from start to finish without crashing or throwing errors.
