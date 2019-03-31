1. This file declares a class, `Player`, instantiates it, and assigns it to a global `player` variable.
2. The `Player` class contains four methods: 
    - `constructor()`
    - `playPause()`
    - `skipTo()`
    - `setVolume()`
3. The `constructor()` method sets initial values for the `currentlyPlaying`, `playState`, `volume`, and `soundObject` properties. 
    - `currentlyPlaying` is set to the first item in `album.songs`. 
    -  The initial `playState` is `"stopped"`. 
    -  The `volume` is set to the number `80`. 
    -  The `soundObject` instantiates a new `buzz.sound` object using the `soundFileUrl` property of `this.currentlyPlaying`. The `buzz` variable doesn't appear to be initialized here, so presumably it's a dependency loaded elsewhere.
4. The `playPause()` method accepts one parameter, `song`. It sets it to `this.currentlyPlaying` by default. It checks to see if `this.currentlyPlaying` is different from `song`, and if so, it:
    - Stops the `soundObject` property.
    - Removes the `"playing"` and `"paused"` classes from the `element` property of `this.currentlyPlaying`.
    - Sets `this.currentlyPlaying` to the function's parameter, `song`.
    - Changes the `playState` property to `"stopped"`.
    - Instantiates a new sound object using `this.currentlyPlaying`, which was just updated to `song`.
5. The playPause() method accepts one parameter, song. It sets it to this.currentlyPlaying by default. It checks to see if this.currentlyPlaying is different from song, and if so, it:
	- Stops the soundObject property.
	- Removes the "playing" and "paused" classes from the element property of this.currentlyPlaying.
	- Sets this.currentlyPlaying to the function's parameter, song.
	- Changes the playState property to "stopped".
	- Instantiates a new sound object using this.currentlyPlaying, which was just updated to song. If the playState property is equal to "paused" or "stopped", then:
	- Sets soundObject property's volume to this.volume
	- Plays the soundObject property
	- Sets the playState property to 'playing'
	- Removes the class 'paused' from the currentlyPlaying property and adds the class 'playing' If not, then:
	- Pauses the soundObject property
	- Sets the playState property to 'paused'
	- Removes the class 'playing' from the currentlyPlaying property and adds the class 'paused'

6. The skipTo() method accepts one parameter, percent. If the playState property is not equal to 'playing', the function:
	- Sets the time of the soundObject property to (percent / 100) multiplied by the duration of the soundObject

7. The setVolume() method accepts one parameter, percent. It sets the volume property to the parameter percent and sets the volume of the soundObject to the parameter percent.
