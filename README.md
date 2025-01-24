#           project:    Dungeon.py
#            author:    Jaxson Santiago <jsantiago2709265@woonsocketschools.com>
#            author:    Kodah Herring <kherring2718138@woonsocketschools.com>
#            author:    Noel Smith <nsmith2718368@woonsocketschools.com>
#           version:    2024.10.25
#       description:    You are a humble traveler wandering throughout villages, you stumble into a bar, you walk in and
#                       overhear something about a treasure hidden deep in a dungeon/cave nearby, peaking your interest
#                       you investigate the dungeon/cave, not knowing what's ahead...

import random, time

spiderHealth = 20
dragonHealth = 100
playerHealth = 15

spiderStrength = 4
dragonStrength = 10


isPlaying = True
while isPlaying:



    print("""
    (You are a traveler that goes around village to village, meanwhile while inside a village you go into a bar, 
    but you overhear a conversation)'I heard that there's treasure at the end of that cave'(one guy says) 'Yeah but
    only a fool would go in there, it's practically a death trap, I had a buddy that went in there... and never
    returned...' (the guy replied, so, intrigued, you investigate said cave, there you meet a merchant, you get a bad 
    feeling about this guy...)
    """)

    time.sleep(1)
    name = input("'Hello there traveler'(says the merchant)'What is your name?' : ")
    time.sleep(1)
    print(f"{name}... that is a fierce and intimidating name...")
    print("""
        'There are ancestries you can pick...' (The Merchant says)
        'The ancestries consist of...
        (Elf)...
        (Dwarf)...
        (Human)...
        (Gnome)...
        (Orc)...
        (Halfling)...
        and (Goblin)...
        Which ancestry would you like to choose?' (The Merchant asks)
            """)
    ancestry = input(" : ")
    time.sleep(1)
    if ancestry == "Elf":
        print("""
        'An elf eh, that's cool, elfs are weak though, but they are very well with magic...' (The Merchant says)
        
        -1 Strength
        +1 Dexterity
        +1 Intelligence
        """)

    elif ancestry == "Dwarf":
        print("""
        'A dwarf, dwarfs are small but kinda strong, they can get around tiny places and spaces, you should be
        happy to be a dwarf' (The Merchant says)
        
        -1 Charisma
        +1 Strength
        +1 Constitution
                 """)

    elif ancestry == "Human":
        print("""
        'Humans are average size, they are different from everyone else in this world, they are in the average when it 
        comes to their attributes, it's a same that they all are going extinct...' (The Merchant says)
        
        +1 attribute point
        """)

    elif ancestry == "Gnome":
        print("""
            'Gnomes are very short creatures, they are weak and frail but are charismatic and have great constitution.'
            (The Merchant says)
            
            -1 Strength
            +1 Constitution
            +1 Charisma
        """)

    elif ancestry == "Orc":
        print("""
            'Orcs are big and strong creatures, they lack intelligence and charisma though, that being the downside of 
            their strength' (The Merchant says)
            
            -1 Intelligence
            -1 Charisma
            +2 Strength
        """)

    elif ancestry == "Halfling":
        print("""
            'Halflings are tiny humanoid creatures that are part human and part elf, they have the resembling skin tone
            and face of a human but also have a small height and pointy ears of a elf, halflings aren't all to strong
            but have great dexterity and wisdom' (The Merchant says)
            
            -1 Strength
            +1 Dexterity
            +1 Charisma
        """)


    elif ancestry == "Goblin":
        print("""
        'Goblins are green mid sized creatures that are quick and deadly, they can either slither their way out of a 
        situation or they could talk their way out of a situation. Here...' (The Merchant reaches into his robe and hands
        you a dagger) 'Keep it, it'll help you on you're journey.' (The Merchant says)
         
         -1 Wisdom
         +1 Dexterity
         +1 Charisma
            """)

    print("""
        (You will soon be given your attributes, these act as something you do during a event, the base amount of
        attribute points for each ancestry is 6, each ancestry also lowers some attributes too, as you see when you get
        your ancestry it says something like -1 Wisdom or +1 Strength, and each ancestry also has one free attribute
        point they can add, you also have speed, speed is what you use to help get away from battles, each
        ancestry's speed is 6, and lastly there is health, base health is set to 15.)
        """)

    if ancestry == "Elf":
        attribute_1 = int(6) - 1
        attribute_2 = int(6) + 1
        attribute_3 = int(6)
        attribute_4 = int(6) + 1
        attribute_5 = int(6)
        attribute_6 = int(6)
        time.sleep(1.5)
        print("""
            'What would you like your free point to be used on?' (The Merchant asks)
            Choice 1 is (S)trength
            and
            Choice 2 is (D)exterity
            and
            Choice 3 is (C)onstitution
            and
            Choice 4 is (I)ntelligence
            and
            Choice 5 is (W)isdom
            and finally
            Choice 6 is (Charisma)""")
        bonusPoint = input(" : ")
        if bonusPoint == "S":
            attribute_1 = 5 + 1

        elif bonusPoint == "D":
            attribute_2 = 7+ 1

        elif bonusPoint == "C":
            attribute_3 = 6 + 1

        elif bonusPoint == "I":
            attribute_4 = 7 + 1

        elif bonusPoint == "W":
            attribute_5 = 6 + 1

        elif bonusPoint == "Charisma":
            attribute_6 = 6 + 1

        time.sleep(1)
        print(f"'You have {attribute_1} Strength'")
        time.sleep(1)
        print(f"'You have {attribute_2} Dexterity'")
        time.sleep(1)
        print(f"'You have {attribute_3} Constitution'")
        time.sleep(1)
        print(f"'You have {attribute_4} Intelligence'")
        time.sleep(1)
        print(f"'You have {attribute_5} Wisdom'")
        time.sleep(1)
        print(f"'You have {attribute_6} Charisma'")

    if ancestry == "Dwarf":
        attribute_1 = int(6) + 1
        attribute_2 = int(6)
        attribute_3 = int(6) + 1
        attribute_4 = int(6)
        attribute_5 = int(6)
        attribute_6 = int(6) - 1
        time.sleep(1.5)
        print("""
            'What would you like your free point to be used on?' (The Merchant asks)
            Choice 1 is (S)trength
            and
            Choice 2 is (D)exterity
            and
            Choice 3 is (C)onstitution
            and
            Choice 4 is (I)ntelligence
            and
            Choice 5 is (W)isdom
            and finally
            Choice 6 is (Charisma)""")
        bonusPoint = input(" : ")
        if bonusPoint == "S":
            attribute_1 = 7 + 1

        elif bonusPoint == "D":
            attribute_2 = 6 + 1

        elif bonusPoint == "C":
            attribute_3 = 7 + 1

        elif bonusPoint == "I":
            attribute_4 = 6 + 1

        elif bonusPoint == "W":
            attribute_5 = 6 + 1

        elif bonusPoint == "Charisma":
            attribute_6 = 5 + 1

        time.sleep(1)
        print(f"'You have {attribute_1} Strength'")
        time.sleep(1)
        print(f"'You have {attribute_2} Dexterity'")
        time.sleep(1)
        print(f"'You have {attribute_3} Constitution'")
        time.sleep(1)
        print(f"'You have {attribute_4} Intelligence'")
        time.sleep(1)
        print(f"'You have {attribute_5} Wisdom'")
        time.sleep(1)
        print(f"'You have {attribute_6} Charisma'")

    if ancestry == "Human":
        attribute_1 = int(6)
        attribute_2 = int(6)
        attribute_3 = int(6)
        attribute_4 = int(6)
        attribute_5 = int(6)
        attribute_6 = int(6)
        time.sleep(1.5)
        print("""
            'What would you like your two free points to be used on?' (The Merchant asks)
            Choice 1 is (S)trength
            and
            Choice 2 is (D)exterity
            and
            Choice 3 is (C)onstitution
            and
            Choice 4 is (I)ntelligence
            and
            Choice 5 is (W)isdom
            and finally
            Choice 6 is (Charisma)""")
        bonusPoint = input(" : ")
        if bonusPoint == "S":
            attribute_1 = 6 + 1

        elif bonusPoint == "D":
            attribute_2 = 6 + 1

        elif bonusPoint == "C":
            attribute_3 = 6 + 1

        elif bonusPoint == "I":
            attribute_4 = 6 + 1

        elif bonusPoint == "W":
            attribute_5 = 6 + 1

        elif bonusPoint == "Charisma":
            attribute_6 = 6 + 1

        time.sleep(1)
        print(f"'You have {attribute_1} Strength'")
        time.sleep(1)
        print(f"'You have {attribute_2} Dexterity'")
        time.sleep(1)
        print(f"'You have {attribute_3} Constitution'")
        time.sleep(1)
        print(f"'You have {attribute_4} Intelligence'")
        time.sleep(1)
        print(f"'You have {attribute_5} Wisdom'")
        time.sleep(1)
        print(f"'You have {attribute_6} Charisma'")

    if ancestry == "Gnome":
        attribute_1 = int(6) - 1
        attribute_2 = int(6)
        attribute_3 = int(6) + 1
        attribute_4 = int(6)
        attribute_5 = int(6)
        attribute_6 = int(6) + 1
        time.sleep(1.5)
        print("""
            'What would you like your free point to be used on?'"
            Choice 1 is (S)trength
            and
            Choice 2 is (D)exterity
            and
            Choice 3 is (C)onstitution
            and
            Choice 4 is (I)ntelligence
            and
            Choice 5 is (W)isdom
            and finally
            Choice 6 is (Charisma)""")
        bonusPoint = input(" : ")
        if bonusPoint == "S":
            attribute_1 = 5 + 1

        elif bonusPoint == "D":
            attribute_2 = 7 + 1

        elif bonusPoint == "C":
            attribute_3 = 6 + 1

        elif bonusPoint == "I":
            attribute_4 = 7 + 1

        elif bonusPoint == "W":
            attribute_5 = 6 + 1

        elif bonusPoint == "Charisma":
            attribute_6 = 6 + 1

        time.sleep(1)
        print(f"'You have {attribute_1} Strength'")
        time.sleep(1)
        print(f"'You have {attribute_2} Dexterity'")
        time.sleep(1)
        print(f"'You have {attribute_3} Constitution'")
        time.sleep(1)
        print(f"'You have {attribute_4} Intelligence'")
        time.sleep(1)
        print(f"'You have {attribute_5} Wisdom'")
        time.sleep(1)
        print(f"'You have {attribute_6} Charisma'")

    if ancestry == "Orc":
        attribute_1 = int(6) + 2
        attribute_2 = int(6)
        attribute_3 = int(6)
        attribute_4 = int(6) - 1
        attribute_5 = int(6)
        attribute_6 = int(6) - 1
        time.sleep(1.5)
        print("""
            'What would you like your free point to be used on?'"
            Choice 1 is (S)trength
            and
            Choice 2 is (D)exterity
            and
            Choice 3 is (C)onstitution
            and
            Choice 4 is (I)ntelligence
            and
            Choice 5 is (W)isdom
            and finally
            Choice 6 is (Charisma)""")
        bonusPoint = input(" : ")
        if bonusPoint == "S":
            attribute_1 = 8 + 1

        elif bonusPoint == "D":
            attribute_2 = 6 + 1

        elif bonusPoint == "C":
            attribute_3 = 6 + 1

        elif bonusPoint == "I":
            attribute_4 = 5 + 1

        elif bonusPoint == "W":
            attribute_5 = 6 + 1

        elif bonusPoint == "Charisma":
            attribute_6 = 5 + 1

        time.sleep(1)
        print(f"'You have {attribute_1} Strength'")
        time.sleep(1)
        print(f"'You have {attribute_2} Dexterity'")
        time.sleep(1)
        print(f"'You have {attribute_3} Constitution'")
        time.sleep(1)
        print(f"'You have {attribute_4} Intelligence'")
        time.sleep(1)
        print(f"'You have {attribute_5} Wisdom'")
        time.sleep(1)
        print(f"'You have {attribute_6} Charisma'")

        if ancestry == "Halfling":
            attribute_1 = int(6) - 1
            attribute_2 = int(6) + 1
            attribute_3 = int(6)
            attribute_4 = int(6)
            attribute_5 = int(6)
            attribute_6 = int(6) + 1
            time.sleep(1.5)
            print("""
                'What would you like your free point to be used on?'"
                Choice 1 is (S)trength
                and
                Choice 2 is (D)exterity
                and
                Choice 3 is (C)onstitution
                and
                Choice 4 is (I)ntelligence
                and
                Choice 5 is (W)isdom
                and finally
                Choice 6 is (Charisma)""")
            bonusPoint = input(" : ")
            if bonusPoint == "S":
                attribute_1 = 5 + 1

            elif bonusPoint == "D":
                attribute_2 = 7 + 1

            elif bonusPoint == "C":
                attribute_3 = 6 + 1

            elif bonusPoint == "I":
                attribute_4 = 6 + 1

            elif bonusPoint == "W":
                attribute_5 = 6 + 1

            elif bonusPoint == "Charisma":
                attribute_6 = 7 + 1

            time.sleep(1)
            print(f"'You have {attribute_1} Strength'")
            time.sleep(1)
            print(f"'You have {attribute_2} Dexterity'")
            time.sleep(1)
            print(f"'You have {attribute_3} Constitution'")
            time.sleep(1)
            print(f"'You have {attribute_4} Intelligence'")
            time.sleep(1)
            print(f"'You have {attribute_5} Wisdom'")
            time.sleep(1)
            print(f"'You have {attribute_6} Charisma'")

    if ancestry == "Goblin":
        attribute_1 = int(6)
        attribute_2 = int(6) + 1
        attribute_3 = int(6)
        attribute_4 = int(6)
        attribute_5 = int(6) - 1
        attribute_6 = int(6) + 1
        time.sleep(1.5)
        print("""
            'What would you like your free point to be used on?'"
            Choice 1 is (S)trength
            and
            Choice 2 is (D)exterity
            and
            Choice 3 is (C)onstitution
            and
            Choice 4 is (I)ntelligence
            and
            Choice 5 is (W)isdom
            and finally
            Choice 6 is (Charisma)""")
        bonusPoint = input(" : ")
        if bonusPoint == "S":
            attribute_1 = 5 + 1

        elif bonusPoint == "D":
            attribute_2 = 7 + 1

        elif bonusPoint == "C":
            attribute_3 = 6 + 1

        elif bonusPoint == "I":
            attribute_4 = 6 + 1

        elif bonusPoint == "W":
            attribute_5 = 6 + 1

        elif bonusPoint == "Charisma":
            attribute_6 = 7 + 1


        time.sleep(1)
        print(f"'You have {attribute_1} Strength'")
        time.sleep(1)
        print(f"'You have {attribute_2} Dexterity'")
        time.sleep(1)
        print(f"'You have {attribute_3} Constitution'")
        time.sleep(1)
        print(f"'You have {attribute_4} Intelligence'")
        time.sleep(1)
        print(f"'You have {attribute_5} Wisdom'")
        time.sleep(1)
        print(f"'You have {attribute_6} Charisma'")


    print("""
    (You walk past the merchant... walking into the cave, the cave is partially lit due to the sunlight seeping in from 
    the beginning of the cave, a torch in hand... you get this nervous chill, do you wish to proceed?)
    Choice 1 is (Yes), to proceed in this journey.
    and
    Choice 2 is (No), and go home, wondering what was in the cave.
    """)
    time.sleep(1)
    proceed = input(" : ")
    time.sleep(1)
    if proceed == "Yes":
        time.sleep(1)
        print("(You take a gulp, going into the cave)")
    elif proceed == "No":
        if ancestry == "Orc":
            print("""
            (You leave the cave forever wondering what the treasure was... you go home... and you lay in your bed,"
            all of a sudden the merchant you saw earlier at the cave entrance bursts into your abode)'YOU WILL BE PUT 
            TO SLEEP FOREVER FOR THE CRIMES OF NOT ADVENTURING THAT CAVE!!!' (The merchant yells, taking out a dagger 
            rushing at you, but you just grab the tiny man by his head, and slam him into the ground)
            
            MEH ENDING?
            """)
            break
        else:
            print("""
            (You leave the cave forever wondering what the treasure was... you go home... and you lay in your bed,"
            all of a sudden the merchant you saw earlier at the cave entrance bursts into your abode)'YOU WILL BE PUT 
            TO SLEEP FOREVER FOR THE CRIMES OF NOT ADVENTURING THAT CAVE!!!' (The merchant yells, taking out a dagger 
            and putting you to sleep for eternity) 
            
            BAD ENDING
            """)
            break

    time.sleep(1)
    print("""
    (You continue into the cave, it is dimly lit due to the torch, you hear dripping, you hear noises too and
    see shadows with several legs walk around you, one of the shadows goes into the lit area around you, revealing...
    SPIDERS!)
    You have two choices
    Choice 1 is (Fight) the spiders, with the chance of losing and end up dying.
    or
    Choice 2 is (Run) away, with the chance of tripping and getting killed by the spiders.
        """)
    time.sleep(1)
    fight = input(" : ")
    time.sleep(1)
    if fight == "Fight":
            roll1 = random.randint(1, 20) + attribute_1
            time.sleep(1)
            sturnOutHealth3 = spiderHealth - roll1
            print(f"You rolled a {roll1}")
            if sturnOutHealth3 > 20:
                time.sleep(1)
                print("(You eviscerate the spiders, leaving no trace of them left)")
                time.sleep(1)

            elif sturnOutHealth3 == 20:
                print("(You slash and hit the spiders until they don't move)")


            elif sturnOutHealth3 <= 19:
                time.sleep(1)
                print(f"You slash and deal {roll1} damage, the spiders now have {sturnOutHealth3} health")
                roll9 = random.randint(1,5) + spiderStrength
                pTurnOutHealth = playerHealth - roll9
                print(f"The spiders attack you and deal {roll9} damage, you now have {pTurnOutHealth}")
                if pTurnOutHealth <= 0:
                    print("(The spiders beat you in combat and tear you piece by piece)")
                    break

                elif pTurnOutHealth > 0:
                    roll10 = random.randint(1,20) + attribute_1
                    aftermathHealth = sturnOutHealth3 - roll10
                    print(f"You rolled a {roll10}")
                    if aftermathHealth < 0:
                        time.sleep(1)
                        print("(You eviscerate the spiders, leaving no trace of them left)")
                        time.sleep(1)
                    elif aftermathHealth == 0:
                        print("(You slash and hit the spiders until they don't move)")

                    elif aftermathHealth > 0:
                        print(f"You slash and deal {roll10} damage, the spiders now have {aftermathHealth} health")
                        roll14 = random.randint(1, 5) + spiderStrength
                        pTurnOutHealth2 = playerHealth - roll14
                        print(f"The spiders attack you and deal {roll14} damage, you now have {pTurnOutHealth2}")
                        if pTurnOutHealth2 <= 0:
                            print("(The spiders beat you in combat and tear you piece by piece)")
                            break

                        elif pTurnOutHealth2 > 0:
                            roll15 = random.randint(1, 20) + attribute_1
                            aftermathHealth3 = aftermathHealth - roll15
                            print(f"You rolled a {roll10}")
                            if aftermathHealth3 < 0:
                                time.sleep(1)
                                print("(You eviscerate the spiders, leaving no trace of them left)")
                                time.sleep(1)
                            elif aftermathHealth3 == 0:
                                print("(You slash and hit the spiders until they don't move)")

    elif fight == "Run":
        roll2 = random.randint(1, 20)
        time.sleep(1)
        print(f"You rolled a {roll2}")
        if roll2 >= 10:
            time.sleep(1)
            print("(You run past the spiders, fleeing them.)")
        else:
            time.sleep(1)
            print(
                "(You trip on a rock, you fall, the spiders catch up to you and start taking chucks and pieces of you.)")
            break

    time.sleep(1)
    print("""
    (You walk deeper in the cave, it gets darker, the air gets thicker, the floor is slippery, you slip and fall, you
    catch yourself on the ledge you look down, you can't see if there is a floor below you due to smoke blocking your vision, 
    do you want to purposely fall, with the chance of either dying or finding a hidden room, or, attempt to pull yourself 
    up, with the chance of slipping and falling?)
    Choice 1 is (No), and pull yourself up from the ledge, with the chance of slipping and falling to your doom.
    and
    Choice 2 is (Yes), and fall into the depths below, with a chance of dying.
              """)
    fall = input(" : ")

    time.sleep(1)
    if fall == "No":
        roll3 = random.randint(1, 20) + attribute_1
        print(f"You rolled a {roll3}")
        if roll3 >= 10:
            time.sleep(1)
            print("(You pull yourself up from the ledge)")
        elif roll3 <= 9:
            time.sleep(1)
            print("(You attempt to pull yourself up but your hands slip and you fall to your impending doom.)")
            break
    elif fall == "Yes":
        roll8 = random.randint(1, 20) + attribute_4
        if roll8 >= 10:
            time.sleep(1)
            if ancestry == "Goblin":
                print("(You have faith, you let go of the ledge falling in the smokey fields below)")
                print("""
                 (You fall down into the deep dark room, seeing a dark room you lift your torch up, you see clues of what
                 might've happened to the human population, you see drawings of goblins, elves, and dwarves killing the human race,
                 you step back in shock, you say to yourself...) 'The merchant? What is he doing to the humans?' (The merchant interrupts)
                 'Well done traveler, you've found out the truth' (He steps from a shadow, revealing that he himself was a goblin, his
                 dark green skin shinning towards you) 'Well traveler, do you wish to join me, and help us with the cause of ending
                 all of humanity?' (The merchant asks you) 'Yes... yes I will...' (You reply) 'Good...' (The merchant says with a smirk
                 growing on his face)

                 ENDING 5: THE ALLIANCE...
                 """)

            elif ancestry == "Human":
                print("(You have faith, you let go of the ledge falling in the smokey fields below)")
                print("""
                 (You fall down into the deep dark room, seeing a dark room you lift your torch up, you see clues of what
                 might've happened to the human population, you see drawings of goblins, elves, and dwarves killing the human race,
                 you step back in shock, you say to yourself...) 'The merchant? What is he doing to the humans?' (The merchant interrupts)
                 'Well done traveler, you've found out the truth' (He steps from a shadow, revealing that he himself was a goblin, his
                 dark green skin shinning towards you) 'Well traveler, you weren't meant to get this far, but now that you have seen 
                 the truth of what happened to you're ancestors, it's time you join them...' (The Merchant says as he unsheathes a sword,
                 you unsheathe your blade, two other men emerge from the shadows, one a dwarf, and the other a elf)'Goodbye traveler,
                 you will never be remembered, you and every on human on this planet.' 
                 

                 ENDING 6: THE TRUTH...
                 """)
                break
            else:
                print("(You have faith, you let go of the ledge falling in the smokey fields below)")
                print("""
             (You fall down into the deep dark room, seeing a dark room you lift your torch up, you see clues of what
             might've happened to the human population, you see drawings of goblins, elves, and dwarves killing the human race,
             you step back in shock, you say to yourself...) 'I-It was them, they're the reason why the human race is going down
             to a handful...' (As you say this, torches get litten in the room, the merchant emerges) 'So... you found out the 
             truth... you weren't supposed to get this far into this cave...' (The Merchant takes his robe off, revealing a green
             body, he looks at you, pulling a sword, but it isn't any ordinary sword, it's the sword of a thousand truths
             this sword can easily slice through anything, could even destroy the Earth if it falls into the wrong hands... the
             merchant points the tip of the sword towards you, two other men emerge from the shadows, they reveal to be a elf and
             a dwarf, they take out swords, the blade sharp.) 'You were a nice man... shame that we have to kill you now that you
             found the truth...' (The merchant says)
    
             ENDING 4: THE SECRET REVEALED...
                     """)
            break
        elif roll8 <= 9:
            time.sleep(1)
            print("(You let go of the ledge, you fall through smoke, and get impaled by spikes)")
            break

    time.sleep(1)
    room4 = random.randint(1, 20)
    if room4 >= 10:
        print("""
        (You walk past the cavern without falling, you walk into the next area of the cave, in this area there are, 
        two doors, one door going north, looking at it gives you this eery feeling, giving you the suggestion not to go
        through it, and a door going south, this door gives you better feeling other then the door to the north,
        which door do you go through?)
        You have two choices
        Choice 1 is The (North) door, a door with a eery feeling, not knowing whats behind it.
        or
        Choice 2 is The (South) door, a door you get a better feeling with, still not knowing what's behind it""")
        time.sleep(1)
        direction = input(" : ")
        if direction == "North":
            time.sleep(1)
            print("""
            You go through the door going north, you take a step forward, you fell nothing below your feet, you fall
            to your death, it was a trap!)
                  """)
            break

        elif direction == "South":
            time.sleep(1)
            print("""(You go through the door going south, along with that you find an item...)""")
            roll16 = random.randint(1,10) + attribute_6
            if roll16 >= 15:
                print("""
                    (You've found a god potion, you take a sip, you feel different..)"
                      
                    FULL HEALTH + MAX HEALTH IS NOW 50
                    """)

                playerHealth = 50

            elif roll16 <= 14:
                print("""
                    (You've found a potion, you take a sip, you feel different..)"
                      
                    FULL HEALTH
                    """)

                playerHealth = 15

    elif room4 < 10:
        print("""
        (You walk past the cavern without falling, you walk into the next area of the cave, in this area there are, 
        two doors, one door going south, looking at it gives you this eery feeling, giving you the suggestion not to go
        through it, and a door going north, this door gives you better feeling other then the door to the south,
        which door do you go through?)
        You have two choices
        Choice 1 is The (South) door, a door with a eery feeling, not knowing whats behind it.
        or
        Choice 2 is The (North) door, a door you get a better feeling with, still not knowing what's behind it""")
        time.sleep(1)
        direction = input(" : ")
        if direction == "South":
            time.sleep(1)
            print("""
            You go through the door going south, you take a step forward, you fell nothing below your feet, you fall
            to your death)
                  """)
            break

        elif direction == "North":
            time.sleep(1)
            print("""(You go through the door going north, along with that you find an item...)""")
            roll16 = random.randint(1, 10) + attribute_6
            if roll16 >= 15:
                print("""
                (You've found a god potion, you take a sip, you feel different..)"

                FULL HEALTH + MAX HEALTH IS NOW 50
                """)

                playerHealth = 50

            elif roll16 <= 14:
                print("""
                (You've found a potion, you take a sip, you feel different..)"

                FULL HEALTH
                """)

                playerHealth = 15

    time.sleep(1)

    print("""
    You walk through the door... you are met with a dark room, you find a switch and flip it, the switch lights
    up the room, you are met with an endless amount of gold but among the gold is a sleeping dragon...)
    You have two choices
    1: (Sneak) past the dragon, but know if you take a wrong step it wakens the dragon.
    or
    2: (Run) past the dragon, taking little to no gold, with the chance of the dragon catching up to you and killing you.
    """)
    time.sleep(1.5)
    sneaky = input(" : ")
    if sneaky == "Sneak":
        roll4 = random.randint(1, 20) + attribute_2
        time.sleep(1)
        print(f"You rolled a {roll4}")
        if roll4 >= 10:
            time.sleep(1)
            print("(You successfully get passed the dragon with a big sack full of gold!)")
            print("""
            (You sneak passed the dragon, you leave the cave, you start to full sprint, both of your hand hold
            sacks filled to the brim with gold, your still running, you make it back to the village, yelling)
            'I SURVIVED, I SURVIVED THE CAVE' (Villagers run out of their houses, some astonished, some confused
            on what the cave is, but you make it home, late at night you fall asleep, but you hear a knock at 
            your door, you open it to find the merchant) 'So you live to tell the tale... too bad you can't tell
            it anymore' (He says as he pulls out a dagger and swings it, but you block it and take it from him, 
            stabbing him in the body, the merchant coughs, but smiles?)'You survived the final test... good... 
            job' (The Merchant takes one final exhale)

            ENDING 1: SNEAKING NOT BROKE AND NOT A JOKE""")
            break
        else:
            time.sleep(1)
            print("""
            (You take a wrong step, you waken the dragon, it looks at you, letting out a fierce roar...)
            You have two choices
            Choice 1 is (Fight) the dragon, with the chance of losing in battle.
            and
            Choice 2 is (Run), taking little to no gold, and with the chance of tripping and dying.
            """)
            time.sleep(1)
            fight = input(" : ")
            if fight == "Fight":
                    strength = attribute_1 * 6
                    roll11 = random.randint(1, 50) + strength
                    time.sleep(1)
                    dturnOutHealth = dragonHealth - roll11
                    print(f"You rolled a {roll11}")
                    if dturnOutHealth < 0:
                        time.sleep(1)
                        print("(You form a black hole and it sucks the dragon in and you win!)")
                        time.sleep(1)

                    elif dturnOutHealth == 0:
                        print("(You smirk, you then say world cutting slash, in a millisecond the dragon is split in half)")

                    elif dturnOutHealth > 0:
                        time.sleep(1)
                        print(f"You slash and deal {roll11} damage, the dragon now has {dturnOutHealth} health")
                        roll12 = random.randint(1, 20) + dragonStrength
                        pTurnOutHealth3 = playerHealth - roll12
                        print(f"The dragon attacks you and deals {roll12} damage, you now have {pTurnOutHealth3}")
                        if pTurnOutHealth3 <= 0:
                            print("(The dragon unleashes a fire from his mouth and turns you to dust)")
                            break

                        elif pTurnOutHealth3 > 0:
                            roll13 = random.randint(1, 50) + strength
                            aftermathHealth2 = dturnOutHealth - roll13
                            print(f"You rolled a {roll13}")
                            if aftermathHealth2 < 0:
                                time.sleep(1)
                                print("(You form a black hole and it sucks the dragon in and you win!)")
                                time.sleep(1)
                            elif aftermathHealth2 == 0:
                                print("(You smirk, you then say world cutting slash, in a millisecond the dragon is split in half)")

                            elif aftermathHealth2 > 0:
                                aftermathHealth4 = roll11 - dragonHealth
                                print(f"You slash and deal {roll11} damage, the dragon now has {aftermathHealth4} health")
                                roll12 = random.randint(1, 20) + dragonStrength
                                pTurnOutHealth4 = playerHealth - roll12
                                print(f"The dragon attacks you and deal {roll12} damage, you now have {pTurnOutHealth4}")
                                if pTurnOutHealth4 <= 0:
                                    print("(The dragon unleashes a fire from his mouth and turns you to dust)")
                                    break

                                elif pTurnOutHealth4 > 0:
                                    roll17 = random.randint(1, 50) + strength
                                    aftermathHealth5 = dturnOutHealth - roll17
                                    print(f"You rolled a {roll17}")
                                    if aftermathHealth5 < 0:
                                        time.sleep(1)
                                        print("(You form a black hole and it sucks the dragon in and you win!)")
                                        time.sleep(1)
                                    elif aftermathHealth5 == 0:
                                        print("(You smirk, you then say world cutting slash, in a millisecond the dragon is split in half)")

                    time.sleep(1)
                    print("(You fight the dragon, slaying it!)")
                    print("""
                    (You slay the dragon, you leave the cave, you start to full sprint, both of your hand hold
                    sacks filled to the brim with gold, your still running, you make it back to the village, yelling)
                    'I SURVIVED, I SURVIVED THE CAVE' (Villagers run out of their houses, some astonished, some confused
                    on what the cave is, but you make it home, late at night you fall asleep, but you hear a knock at 
                    your door, you open it to find the merchant) 'So you live to tell the tale... too bad you can't tell
                    it anymore' (He says as he pulls out a dagger and swings it, but you block it and take it from him, 
                    stabbing him in the body, the merchant coughs, but smiles?)'You survived the final test... good... 
                    job' (The Merchant takes one final exhale, take in what just happened, your superstitions were
                    correct about this guy...)

                    ENDING 2: BRAWLING NOT BROKE AND NOT A JOKE""")
                    break


            elif fight == "Run":
                roll7 = random.randint(1, 20) + 6
                time.sleep(1)
                print(f"You rolled a {roll7}")
                if roll7 >= 10:
                    time.sleep(1)
                    print("(You out run the dragon!)")
                    print("""
                    (You run and keep running, you have little to no gold in hand, but you escape the cave, your still 
                    running, you make it back to the village, yelling)'I SURVIVED, I SURVIVED THE CAVE' (Villagers run out of
                    their houses, some astonished, some confused on what the cave is, but you make it home, late at night you
                    fall asleep, but you hear a knock at your door, you open it to find the merchant) 'So you live to tell the
                    tale... too bad you can't tell it anymore' (He says as he pulls out a dagger and swings it, but you block it
                    and take it from him, stabbing him in the body, the merchant coughs, but smiles?)'You survived the final
                    test... good... job' (The Merchant takes one final exhale)

                    ENDING 3: FLEEING BROKE BUT NOT A JOKE""")
                    break
                else:
                    time.sleep(1)
                    print("(The dragon catches up to you, eating you whole.)")
                    break

    elif sneaky == "Run":
        time.sleep(1)
        print("(You run past the dragon! He wakes up and tries to eat you)")
        roll6 = random.randint(1, 20) + 6
        time.sleep(1)
        print(f"You rolled a {roll6}")
        if roll6 >= 10:
            time.sleep(1)
            print("(You out run the dragon!)")
            print("""
            (You run and keep running, you have little to no gold in hand, but you escape the cave, your still 
            running, you make it back to the village, yelling)'I SURVIVED, I SURVIVED THE CAVE' (Villagers run out of
            their houses, some astonished, some confused on what the cave is, but you make it home, late at night you
            fall asleep, but you hear a knock at your door, you open it to find the merchant) 'So you live to tell the
            tale... too bad you can't tell it anymore' (He says as he pulls out a dagger and swings it, but you block it
            and take it from him, stabbing him in the body, the merchant coughs, but smiles?)'You survived the final
            test... good... job' (The Merchant takes one final exhale)

            ENDING 3: FLEEING BROKE BUT NOT A JOKE""")
            break
        else:
            time.sleep(1)
            print("(The dragon catches up to you, eating you whole.)")
            break
