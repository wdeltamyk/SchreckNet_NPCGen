# VTM5E NPC Generator

This is a simple NPC generator for VTM5E. It uses a Python GUI to generate an NPC on the fly within seconds.
The names are determined via a pull from BehindTheName.com. As such you will need a valid API key and to place it inside of the .env file.
The stats are pulled from the Schrecknet JSON files. This is an otherwise unrelated project but I've created a fork so the original authors are given proper attribution.

## Names

The names that can be pulled include, ancient, modern and mythological/religious.
A first name will always be made, a last name will be attempted but should the culture not have a last name, it will be skipped. With only the first name being returned.

## Options

1. Generation: As is lore to the World of Darkness, the lower the generation the stronger the kindred, this affects blood potency.[^1]
2. Clan: Rather obviously, setting this sets the clan and disciplines available.
3. Skill Focus: Right now this is set to three options, Social, Mental and Physical. I will be expanding this into a more robust system in the future, allowing mutiple attributes to be selected as a focus, thus affecting skill distribution.
4. Sect: Ranges from Camarilla, Anarchs, Autarkis/Independent, Sabbat, Hecata, Black Hand[^2], and Ashirra.
5. Diablerist: Setting this to "Yes" will grant the generated NPC a random non-clan discipline, setting it to "No" ignores the value.
6. NPC Importance: Right now the only values that make a difference are: Thug, Minor, Important, Boss and Big Bad, there are two additional values which are not yet implemented but will be shortly, these values are: Ancienct[^3] and Mythical[^4].
7. Culture: This is what determines the name of the NPC generated. Playing around with this you will see there are hundreds of options. Some cultures have a last name, some do not.
   A very few amount of these will cause name generation errors, I don't have a comprehensive list but I've only come across one so far, which I forgot to note down.

## Considerations

1. Gender is determined randomly for now, I will be including an option to set this for more reliable NPC generation.
2. The skills are distributed randomly, attributes are distributed based on the option for Skill Focus you choose, this is an unintended bug that I'll be fixing shortly.

[^1]: Generation 2 has been left as an option despite no second generation vampires existing as per the World of Darkness lore, this is solely for storytellers who wish to ignore the lore and it's easy enough to skip over if you're sticking to the lore. Generation 1 has also been included if you wish to include Caine as an NPC. As of right now only Generation 16 to 8 make a difference. I will be adding more benefits for lower generations and for Generation 1-3, will be adding a default blood potency of 10 for these options. I will also be adding an age option for the NPCs, the longer you've been a kindred the higher your blood potency will generate toward, right now it's a random value.
[^2]: The Black Hand is, in the lore, a defunct sect. I am running my game in a way that the Black Hand have been reformed, if you're wanting to stick strictly to a modern setting that doesn't alter the lore, ignore this option.
[^3]: Ancient NPCs will have nearly perfect stats, and will have nearly perfect mastery of their clan disciplines. These will be Methuselahs or kindred who have devoted themselves entirely to mastery through various magics (blood magic, oblivion ceremonies) or diablerie of lower generation vampires. Not quiet perfection but close, and more or less unkillable by players, at least solo and definitely in their earlier levels.
[^4]: Mythical NPCs, Antediluvians, Second Generation, Caine. Perfect stats, perfect mastery of their clan disciplines, and are unkillable by players (presumably).

## Installation

The packed exe file is ready to use.
There are no additional requirements beyond Python - all dependencies are included with the latest Python releases, I specifically built this with Python 3.12. Should any dependencies fail to build though I have included a requirements.txt file.
To build the requirements simply run: python -m pip install -r requirements.txt
This will likely not be needed though.
