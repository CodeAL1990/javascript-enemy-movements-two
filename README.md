# javascript-enemy-movements-two

Moved previous work from enemy-movements-one to this to start editting for movement type two
Change the source to movement two image and change the spriteWidth and spriteHeight to match the sprite's dimensions
Uncomment this.speed and change the range of pixels from 1 to 5
Change x in update to a decrement of this.speed which will make the sprites go left
Comment y for now and add an if condition when x + width is less than 0 (meaning once the sprite fully disappears) x will be assigned to canvas.width which will reset the sprite to the right due to 500px width
Using a combination of math methods such as Math.sin and Math.cos, you will now try to create a 'sine wave' movement type
To create a this wave, you'll need to pass in a value (in this case 0) to Math.sin and move it constantly through values -1 to 1 to create a geometric wave
Add a new property called angle in the constructor and set it to 0
In update for y, uncomment it and increment it by Math.sin(this.angle)
Now increment angle by 0.1 to see a slight wave in the sprite movement
Change angle to Math.random() \* 2 for now
To randomise movement speeds, add a property called angleSpeed to constructor and assign its value to Math.random() \* 0.2 for eg
Remove hardcoded value of the increment in angle and replace it with angleSpeed
Set angle in constructor back to 0
Change width and height in constructor to the sprite's dimension divided by 2 instead of 2.5 to make it bigger
To make the 'sine wave' more visible, instead of going through the values between -1 and 1, you can multiply by the increment of y in update by a number (3 \* Math.sin...) to have y move through the values between -3 to 3 instead, resulting in a bigger arc
To give more variations to 'arc', add a property of curve in constructor randomised between 0 and a number you choose (Math.random() \* number), and replace the hardcoded value of y in update to this.curve
'Sine wave' movement type two is done!
