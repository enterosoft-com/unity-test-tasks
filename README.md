<p align="center"><img src="https://user-images.githubusercontent.com/91733173/233398396-32598703-3cb6-4e60-8ebb-d7293ef46188.png" width="250"></p>


# Community
[<img src="https://assets-global.website-files.com/6257adef93867e50d84d30e2/636e0a6a49cf127bf92de1e2_icon_clyde_blurple_RGB.png" height="30">](https://discord.gg/HqbPAwE6) &emsp; [<img src="https://lh3.googleusercontent.com/0rpHlrX8IG77awQMuUZpQ0zGWT7HRYtpncsuRnFo6V3c8Lh2hPjXnEuhDDd-OsLz1vua4ld2rlUYFAaBYk-rZCODmi2eJlwUEVsZgg" height="30">](mailto:career.unity@enterosoft.com) &emsp; [<img src="https://lh3.googleusercontent.com/3_OFn2skqHXk-UQ-9RUdNrDl_HQJrMCxks5teQcUrF_bOSeDG1hD8j83FeD31W8hASZCvubzsGfumuJq8kvvSAq03wY87RZ7Otx_DF4" height="30">](https://www.youtube.com/@enterosoft7018/featured)

# Introduction

It is suggested to use the recommended LTS version of Unity.

⭐ - more difficult task

After completing the tasks, send the "Assets" folder by [e-mail](mailto:career.unity@enterosoft.com) (this can also be a github link)

# Preparing the project

1. Create a new project **3D Core**
2. Clear the Assets folder
3. Add these files - [Assets/\_Project](https://github.com/enterosoft-com/unity-test-tasks/tree/master/Assets)
4. Install from Package Manager **2D Sprites**
5. Open the "Game" scene

# Basic Movement - Player Prefab

1. Add object "_PlayerCube1_" and change position **Y = 3** and rotation **Y = 90**
2. Write a move script for it
  - Constant **velocity** as well **Z = 10**
  - When touching the screen / clicking the left mouse button, the object jumps up using **impulsive force Y = 18.6**
  - Gravitation **y-axis** should be **-60**
3. Write a follow object script for the camera
  - Position offset **Vector3(7,4.5,-4)**
  - Rotation **Vector3(30,-45,0)**
  - Smoothness effect can be added
4. In [_Video_](https://drive.google.com/file/d/1bS-ooH_PQ0u9zm9nHMOl24CeLgS7SnyI/view?usp=share_link) it is shown how the final effect should look like (I added a few cubes in the background to show the movement)

# Map building

1. Create prefabs from the following objects, give them material, write and add a script that stores the ID ![Image5](https://user-images.githubusercontent.com/91733173/233374440-c12320af-daec-42fe-b21c-637a4d32708b.png) **it is important that the prefabs have the appropriate ID**
2. 6 cubes (ID in sequence: **3,4,5,6,7,8** ) ("Cubes" material) ![Image6](https://user-images.githubusercontent.com/91733173/233379041-7207a9df-e36b-48cf-a7ff-f655c256a1a8.png)
3. Coin (id: **1** ) (material "Coin")
4. Spike (id: **2** ) (material "Trap")
5. Prefab "Finish" (id: **0** ) trigger 1x5x1 with transparent texture on the floor (create material):<img src="https://user-images.githubusercontent.com/91733173/233377000-19903851-2b85-4a60-8421-14ba4c85c4f3.png" height="200">


6. Build a simple, short map by placing each type of prefabs and finally finish.

#

# Collision Detection

1. When a player collides with a wall or a spike, he starts from the starting position - **Vector3(0,3,0)**
2. Destroys a Coin if it touches it
3. When it hits Finish, the player stops
4. Example in [_Video_](https://drive.google.com/file/d/1v8RFOXAh2qEMrFIpfR1VqijOSoWWrS6W/view?usp=share_link)

# Menu UI

Change scene to "Menu"

1. Using the graphics included in the project, create the following menu:

- Use the Assets/\_Project/Resources/Creepster-Regular font
- The button background needs to be edited accordingly **Sprite Editor**
- The 3 icons at the bottom do nothing, buttons **PLAY** and **ONLINE** go to the next windows

![Image1](https://user-images.githubusercontent.com/91733173/233378860-54a72d54-370f-4a88-a475-a1b7b9d0bb59.png)


2. Window when pressed **PLAY** :

- the top left will show the number of coins, but that's later,
- the middle button shows the loading screen (it's lower) and changes to the scene **"Game"**
- button on the bottom right that takes you back to the main menu


![Image8](https://user-images.githubusercontent.com/91733173/233378808-7ca0d99f-00e7-4eaa-ae02-aa68fe91490c.png)


3. Window when pressed **ONLINE** :

- There's a button in the middle that doesn't do anything
- button on the bottom right that takes you back to the main menu

![Image9](https://user-images.githubusercontent.com/91733173/233378777-91b93a2a-d240-48e6-9b13-7a8649a5b035.png)


4. And a loading screen saying loading:

![Image2](https://user-images.githubusercontent.com/91733173/233378702-fac045de-aca9-4df9-b364-f9182e303642.png)


# Game UI

1. During the game:

- Add text to coins (text itself, functionality later) and a pause button

⭐ Add protection so the cube doesn't jump when pressing pause

![Image3](https://user-images.githubusercontent.com/91733173/233379399-aaea6f6c-c572-420a-bf00-3e887c24c5c3.png)


2. Menu Pause:

- tinted background
- title

- button to continue
- return to menu button

![Image10](https://user-images.githubusercontent.com/91733173/233379435-57a23214-842e-4526-a306-fc8a645a70cf.png)


3. Game over screen:

- change the scripts so that the cube disappears after losing and GAMEOVER appears on **2 seconds** , after this time the game starts again

![Image11](https://user-images.githubusercontent.com/91733173/233379487-6f13087e-ea8b-4026-a88e-01fe93e5bae7.png)


4. Win screen:

- title
- return to menu button

![Image4](https://user-images.githubusercontent.com/91733173/233379537-577c298b-649e-4652-bac1-ea19798238c0.png)


# Data storage

1. Save the number of coins collected (display them in the menu and in the game)
2. Save the number of deaths

# Audio

1. Add a click sound to each button (Assets/\_Project/Audio/button.mp3)
2. Add coin collect sound (Assets/\_Project/Audio/Gem collect.mp3)
3. Add in-game music (Assets/\_Project/Audio/extreme-sport-trailer-125729.mp3)

# ⭐ Level save system

The goal is to save the map as **JSON** to the file. In the editor it should be possible to set " **musicUrl**" " **levelAuthor**" " **levelDescription**" " **levelName**" " **levelVersion**"

Also add a button in the editor that will trigger the map save.

1. The JSON structure must look exactly like this:
```json
{
  "musicUrl": "",
  "levelAuthor": "",
  "levelDescription": "",
  "levelName": "",
  "levelVersion": "",
  "levelObjects": [
    {
      "id": 7,
      "isStatic": false,
      "position": {
        "x": 0.5,
        "y": 1.75,
        "z": 1.5
      },
      "rotation": {
        "x": 0.0,
        "y": 0.0,
        "z": 0.0,
        "w": 1.0
      },
      "scale": {
        "x": 1.0,
        "y": 1.0,
        "z": 1.0
      }
    }
  ]
}
```

2. Save path $"{Application.dataPath}/Levels/{levelName}.json"
3. Save the level

# ⭐ Loading a level from a file

Button in the menu: **PLAY** -\> <img src="https://user-images.githubusercontent.com/91733173/233379666-af6aeb1d-a306-4a57-8555-e931380be7ad.png" height="50">
 loading a previously saved level from a file.

# ⭐ Level loading from internet

Button in the menu: **ONLINE** -\> <img src="https://user-images.githubusercontent.com/91733173/233379746-b183ea67-fcbe-49ce-9fce-152443dbbdfb.png" height="50">
 loading the level from this link using htttp

[https://storage.googleapis.com/enterosoft-data/Level1.json](https://storage.googleapis.com/enterosoft-data/Level1.json)

(with music, link provided in json)

#

After completing the tasks, send the "Assets" folder by [e-mail](mailto:career.unity@enterosoft.com) (this can also be a github link)
