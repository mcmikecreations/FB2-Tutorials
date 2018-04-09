# Endless Battle
A simple C++ Builder OpenGL game created by @mcmikecreations.
[Youtube video](https://youtu.be/JhBnjKI4LR0)
![Endless Battle](https://i.imgur.com/eMiHD4y.png)
## Game Logic
There are two kinds of entities in the game: the player and the enemies.
The enemies can be divided into 3 types:
1. A standard one that moves in a spiral.
2. A fast one that jumps towards the player.
3. A slow one the moves straight to the player.

![Enemy AI](https://i.imgur.com/4ugkGNi.png)
Every entity (including the player) has its own speed, health and so on. The player also has a score and can see an indication of an enemy coming from outside the screen. In addition, every entity can have multiple particle systems attached.
![Indicators and effects](https://i.imgur.com/5iO4yix.png)
Every killed enemy explodes leaving a nice particle trail behind.
The player can kill an enemy using a "Beam Weapon". It is a beam that charges and depletes over time, so you have to consider your timing of every shot. Also, it can destroy multiple enemies at once. For maximum effect, the player can swing the beam all over the map to deal damage to as many enemies as possible.
Since the task for me was to develop the game using VCL in C++ Builder, I used a ShowMessage dialog to show the controls.
![Beam Weapon and VCL](https://i.imgur.com/SxJqnHq.png)
## Uses
Here is a list of everything that the game uses.
### Libraries
All these things should come with C++ Builder, but I'll still list them in case something goes wrong.
- OpenGL
- GLAUX
- VCL
- std::vector
- mmsystem.h

### Textures
Here's the source of all the textures I use.
- Space Ships: [OpenGameArt.Org](https://opengameart.org/content/spaceships-1)
- Alien from the logo: [ahookamigurumi.com](http://www.ahookamigurumi.com/bavoirs-pour-bebes-geek-space-invaders/)
- Everything else was made by me

### Sounds
- Explosion: [freesound.org](https://freesound.org/people/timgormly/sounds/170144/)
- Music: [dl-sounds.com](https://www.dl-sounds.com/royalty-free/fast-ace/)
- Don't know how it got there but I'm too lazy to re-upload all of the archives. [Hundred Beanie Dreams from soundcloud.com](https://soundcloud.com/zaylien/h3h3)

### Fonts
- LCD Solid: [fontspace.com](http://www.fontspace.com/lcd-solid/lcd-solid)

### Additional info
- [Entity collision](https://en.wikipedia.org/wiki/Elastic_collision)
- [Circle-Box collision](https://stackoverflow.com/questions/401847/circle-rectangle-collision-detection-intersection?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa)
- [C++ Builder OpenGL Setup](http://edn.embarcadero.com/article/10528)

## Texture creation
All of the textures were made using a raster graphics editor. Every texture is a bmp file, that has four channels: RGB and Alpha. Alpha was mostly drawn by hand, so there are a few bad spots here and there.
The game doesn't take depth into account, because that will screw the default shader, so you have to keep texture order in mind.
## Sound creation
As far as I remember, the game is most comfortable with .wav file format, but it doesn't use an Audio Mixer, so it is limited to one sound at a time. I chose music to be that sound, but you can modify everything if you want to include an Audio Mixer.
