#Using and Playing sound in Open Frameworks

Learning Goals: Become familiar with the sound player in Open frameworks and create an example of using sound with Arduino. 

In class demo: Create a simple fft visualization using a sound click 

###Assignment

For homework 

1. Please review chapter 5 of Mastering openFrameworks: Creative Coding Demystified. 

2. Also create a physical interface prototype for a childrens museum. Your installation needs to teach children about the doopler. 
About the Doppler effect: 
https://www.google.nl/webhp?sourceid=chrome-instant&ion=1&espv=2&ie=UTF-8#q=doppler%20effect


#####What is a sample? 
A sound sample is an array of samples with a number of channels and a time step. 

#####How do you play sound? 
In OF you can play sound using the ofSoundPlayer class. 
To load a sound sample: 

	//in setup
	ofSoundPlayer sound; 
	sound.loadSound(fileName); 
	//in update call the global update function for the sound engine
	ofSoundUpdate(); 
	sound.play()
	

A few useful functions: 

`sound.stop()`
stops a playing sound

`sound.setPosition(pos)` sets a sound position where 0 is the start and 1 is the end. 

`sound.setPositionMS(ms)` sets sound in milliseconds 

`sound.getIsPlaying()` returns true or false 

`sound.setPaused(pause)`pauses a clip

`sound.stop` stops a clip

`sound.setLoop(looping)` enables / disables looping

`sound.setMultiPlay(multi)` VERY important. Allows a sound to be played multiple times at once

`sound.getPosition()` gets position of playing clip in a val of 0 to 1 

`sound.getPositionMS()` gets position sound in milliseconds 

more functions of the new sound object we made above include 
`.setSpeed(speed) `

`.setVolume(vol)` use a 0-1 val

`set.Pan(pan)`  use  -1 for left and 1 for right 

more functions here: 
http://openframeworks.cc/documentation/sound/ofSoundPlayer.html#show_setMultiPlay

Global functions we need to know about: 
`setSoundVolume(vol)` changes volume for all playing sounds
`ofSoundStopAll() `


http://openframeworks.cc/documentation/sound/ofSoundStream.html

http://www.fmod.org/



