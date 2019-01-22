# Auto-Target
Auto-Target and finish your skill in PVP and PVE</br>
**This module require keyFile for enable**</br></br>
![](autoTarget.gif)</br>

# Commands
```
- at on             #enable
- at off            #disable
- at reload         #reload the config file
```
# Config.json
```
{
    "enabled": true,                          #enable and disable this module
    "markTarget": {                           #put arrow mark on target head follow job/class ***
        "Alliance": {                         #0 = red color
            "0": [],                          #1 = yellow color
            "1": [],                          #2 = blue color
            "2": []
        },
        "Enemy": {
            "0": [],
            "1": [],
            "2": []
        }
    },
    "lockNpc": [huntingzone_npcId],           #lock on npc like world boss *array
    "lockBuff": [buffId],                     #lock on enemy by buffId *array
    "skills": {                               #config for lock on skill
        "4": {                                #read in job/class ***
            "20": {                           #skill id *can get from skill-prediction preset for id
                "name": "Flaming Barrage",    #skill name
                "target": [                   #read in target tags *array ***
                    "enemy-all",
                    "boss"
                ],
                "dist": 35,                   #max skill distance *meter
                "maxTarget": 1,               #max lock on target
                "lockSpeed": 50,              #lock speed *if ghost should increase this
                "castSpeed": 150,             #cast speed *if ghost should increase this
                "autoCast": true              #enable and disable auto cast for skill *require castSpeed
            }
        }
    }
}
```
# Job / Class
```
0 = warrior           7 = mystic
1 = lancer            8 = reaper
2 = slayer            9 = gunner
3 = berserker         10 = brawler
4 = sorcerer          11 = ninja
5 = archer            12 = valkyrie
6 = priest
```
# Target Tags *Priority sort
```
- boss            #lock on boss monster *detect by boss hp gauge
- npc             #lock on npc *require lockNpc
- enemy-healer    #lock on enemy healer near you *PVP
- enemy-buff      #lock on with enemy buff *require lockBuff - PVP
- enemy-all       #lock on all enemy near you *PVP
- member-clean    #clean party member *only mystic
- member-heal     #heal member *only priest and mystic
```
# Q & A
Q: what is keyFile</br>
A: keyFile is system to bind script on computer make it cannot share</br>
</br>
Q: it generate keyFile for me but not work</br>
A: you need send that keyFile to me for make it active</br>
this script so much effect in PVP so it not public lol~</br>
