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

## Guardian Clicking [^bronze]
At the top of the loop is **Guardian Clicking**. This is easily the most simple, fundamental feature. Depending on which Guardian you've chosen the bot will click differently. If you've chosen the `Fairy` guardian, it'll click `100 times` before moving on. The `Dragon` guardian is rate-limited. He can only fire once every second. For that reason, if you've chosen the `Dragon` guardian, it'll click `15 times` in one second intervals before moving on.

## Party Upgrades [^bronze]
Next up the bot will open the upgrades panel and check to see if you can afford any upgrades. If so, it will buy any and all you can afford working from the top-down.

## Gold Farming [^bronze]
The bot will check to see if you "hit a wall" by checking for the `Fight Boss` button that appears when you've lost a boss fight. 

## Chests [^silver]
Once every two hours the bot will open the inventory panel and check to see if you have any chests to be opened. If so, it'll loop through each chest `Common >> Epic`. Other versions of chests will be implemented soon.

## Guardian Training [^silver]
Every five minutes the bot will check the *Hall of Magic* to see if your guardian's training is off cooldown. If it is, it'll start a new round of training.

## Tavern Cards [Coming Soon] [^silver]
A feature I'm planning on implementing soon is to have the bot purchase as many tokens as it can, and then open as many tavern cards as it can afford.

## Map Missions [^gold]
The bot opens up the map and uses OCR to see how many troops you have available. If you have at least one troop available it will start working through a preset list of mission spawnpoints. If it successfully finds a mission node it will start the mission. It will keep doing this until there are no troops left. 

The bot will then periodically check the map to make sure all troops are being used and claim any completed missions.

## Guild Expeditions [^gold]
Opens up the guild expeditions screen and checks to see if we need to claim an expedition. If so, claim it and start a new one. It will then use OCR to read the mission timer and see how long until the expedition should complete. It will remember when the expedition should be completed and only check back when it reaches that time. 

If there are no more expeditions available, it will check how long until they refresh and check back at that time.

## Auto Prestige [^gold]
Periodically check the Prestige screen to see if you've reached the multiplier you chose in the options panel. If so, choose the **FREE** prestige option and wait a moment until the game processes it. 

Once we've started over, use the guardian to farm some gold for a cycle. Assuming you have enough gold, the bot will purchase all `5` party slots and setup your party based on the choices you made in the options panel. 

!!! note
    If you didn't change the party configuration, the bot will use the default values which are 1. Boris > 2. Solaine > 3. Burt > 4. Benedictus > 5. Blaze
    
[^bronze]: Requires at least the (BRONZE Edition)
[^silver]: Requires at least the (SILVER Edition)
[^gold]: Requires the (GOLD Edition)