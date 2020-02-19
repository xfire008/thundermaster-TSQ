# thundermaster-TSQ
Intelligent randomizer for Thunderstone Quest

INTRODUCTION
I am an avid boardgamer, amateur programmer, and new GitHub user. I enjoy thinking up utilities to improve the play experience of games that I love, particularly programs that assist with setup or component randomization. I have XML experience, but no formal instruction in most other common programming languages. One of my favorite recent games is Thunderstone Quest, and I set out to repurpose an older (and quite fine randomizer) developed by a gentleman named Erv Walters for the first two editions of the game. Using my limited knowledge, I altered fields and added card data sets and conditions to "app.js" to update the original randomizer for the new version of the game. For the most part, it works quite well, but there are kinks I just cannot seem to work out - some of these appear to be related to cached data on different browsers, while others are just beyond my capacity to figure out. And that is why I'm here - I would be most grateful for any assistance! 


NOTES ON DEVELOPMENT:
My first step in rebuilding Thundermaster was to identify features of the utility that no longer served any purpose in Thunderstone Quest (hereafter, TQ) but that could be reconfigured to support the new features of the game, namely Dungeon Tiles, Modular Variants, and Barricades Mode.

The obsolete fields were Traps, Treasures, Diseases, Thunderstones, and Settings. Traps, Treasures, and Diseases made the most sense to convert to the Dungeon Tile fields, as their properties were very lightly embedded and had few dependencies. I chose to make each of these fields correspond to a particular level dungeon tile because I lack the knowledge to replicate what Erv did with the monster randomizer. Ideally, you could have one function that spits back two tiles of each level.

Settings converted quite nicely to Modular Variants and I left Thunderstones present but dormant in the utility in the event that it needed to be repurposed at a later time. For most of the card functions, I renamed attributes to correpond to the lexicon of TQ, so 'strength' became skill, 'disease' became 'wound' etc. Certain functions also no longer had significance in TQ, such as matching for diseases/wounds - these can be destroyed as Village actions and Clerics are always part of the hero setup. I also created at least a half dozen functions for new TQ cards and game properties, including dependencies on certain hero races, cards requiring discard outlets to work, and other functions.  
 

KNOWN BUGS:
-toggle button at top only displays "Barricades Mode" in Firefox; it displays as "Solo Game" in other browsers. Why?

-"Village Type Limits" toggle button should default to "Allowed" on load

-define proper instructions for randomizer to select one hero from each class during setup. This is currently achieved by adding requirements to monster groups, a functional but far less elegant approach

-"Display Set Codes" and "Monster Levels 1,2, & 3" buttons do not work and set codes do not appear on card names in Chrome

-Internet Explorer and MS Edge briefly load what appear to be an old cached version of the original Thundermaster before loading the new version

-Internet Explorer, MS Edge, and Firefox seem to save the previous configuration on reload; Chrome does not

-the card Lilande Songweaver needs a function that ties it to side quests/prestige classes

-a link to contact Erv Walters remains on the page. I have no idea how to remove this - where is this information even coming from exactly? 

**if you have any comments for improvement or can directly fix these issues, please contact me here on GitHub. Do not email Erv Walters (whose contact info is still embedded in the app) unless he explicitly mentions that he wants to be involved in this effort**   

-----------------------------------------------------------------------------------------------------
GAME USE INSTRUCTIONS (Firefox):
-for a typical game of Thunderstone Quest, do the following:
1) Toggle "Village Type Limits" to ALLOWED; toggle "Barricades Mode" to ALLOWED or DISALLOWED as desired
2) Toggle sets as necessary to correspond to the TQ expansions that you own
3) Under "Variants", toggle "Solo Game" to REQUIRED or DISALLOWED as desired, then set drop-down as desired 
4) Set the values on the three "Dungeon Tiles" drop-downs to "2"
5) Set the value on the "Guardian" drop-down to "1"
6) Click the "Randomize" button at the top and you're good to go!


ADDITIONAL NOTES:
-selecting "Barricades Mode" will automatically eliminate Side Quests as a variant option
-selecting "Solo Game" REQUIRED under "Variants" will automatically adjust the quantity of Hero stacks to 2 and quantity of Village stacks to 4
-all card names are English only at the moment; I'm happy to provide instructions if someone wants to do French or German translations for input

*if using Internet Explorer or MS Edge, you may see an old cached version of Thundermaster load before the new version. No idea why this is
*if using Chrome, you will not see set codes and the "Display Set Codes" and "Monster Levels 1,2, & 3" toggles at the top do not function. Additionally, the "Barricades Mode" button displays as "Solo Game". No idea why this is    
-----------------------------------------------------------------------------------------------------

CREDITS
Design of the original Thundermaster randomizer is credited to Erv Walters. Chris Hartten altered this randomizer for use with Thunderstone Quest in July 2019. Thunderstone and Thunderstone Quest are trademarked properties of the Alderac Entertainment Group (AEG).  

  
