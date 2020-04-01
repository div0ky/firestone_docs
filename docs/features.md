# Feature Breakdown
Here I list out all of the bots features, how it works, and its expected behavior. 
        
* Bronze Edition
    - Upgrades
    - Farming
    - Clicking
* Silver Edition
    - Chests
    - Guardian Training
    - Tavern Cards
* Gold Edition
    - Map Missions
    - Guild Expeditions
    - Auto Prestige
    
!!! note
    Each edition is cumulative. Silver includes all the Bronze features and Gold includes all the Silver & Bronze features.
   
## Summary
The bot runs on a primary loop. It processes each feature in turn and then cycles back around to the top ad nauseam.

## Guardian Clicking
At the top of the loop is **Guardian Clicking**. This is easily the most simple, fundamental feature. Depending on which Guardian you've chosen the bot will click differently. If you've chosen the `Fairy` guardian, it'll click `100 times` before moving on. The `Dragon` guardian is rate-limited. He can only fire once every second. For that reason, if you've chosen the `Dragon` guardian, it'll click `15 times` in one second intervals before moving on.

## Party Upgrades
Next up the bot will open the upgrades panel and check to see if you can afford any upgrades. If so, it will buy any and all you can afford working from the top-down.

## Gold Farming
The bot will check to see if you "hit a wall" by checking for the `Fight Boss` button that appears when you've lost a boss fight. 

## Chests
Once every two hours the bot will open the inventory panel and check to see if you have any chests to be opened. If so, it'll loop through each chest `Common >> Epic`. Other versions of chests will be implemented soon.

## Guardian Training
Every five minutes the bot will check the *Hall of Magic* to see if your guardian's training is off cooldown. If it is, it'll start a new round of training.

## Tavern Cards [Coming Soon]
A feature I'm planning on implementing soon is to have the bot purchase as many tokens as it can, and then open as many tavern cards as it can afford.

## Map Missions
[COMING SOON]

## Guild Expeditions
[COMING SOON]

## Auto Prestige
[COMING SOON]