#Lynda Green-Sock Tutorial

Last updated: 2016.JAN.14 1:57pm

Tutorial for Green-Sock animation library.

###Links

[Lynda: Creating a HTML5 Banner Ad with GreenSock](http://www.lynda.com/HTML-tutorials/Adding-background-clouds/373558/420197-4.html)

###Steps

1. Create 'Outer' container with a hyperlink
2. Create 'Inner' container to house all elements

#### For sprites

- **define sprite dimensions:** <br>
```width: 60px;``` <br>
```height: 95px;``` <br>

- **move background image to zero out:** <br>
```background-position: -243px -230px;``` <br>

- **position sprite:** <br>
```top: 90px;``` <br>
```left: 290px;``` <br>


###Additional notes

- Use single PNG as a sprite sheet (seemingly instant loading)
- Compress to PNG-8


- ```myAd_Img``` class defines the base style, graphic, and position.
- each individual element should have their own unique IDs.

- don't use any HTML tag elements, just in case the page the banner sits in has styles already.
- Use all custom div tags.

- use Timeline feature of GreenSock library so you can easily chain animations.
	- ```tl1.from('#<div_id>', <seconds>, { <property>: <value>, ease: <ease function (Power2.easeOut, etc) >}, '-=<time offset>' );```

- animations can be chained using dot syntax '.'.

- can also be named
- can 'seek' to a certain 'name' tag, and you can preview your animation at that point.
	- ```<timeline>.seek('<name>');```

- declaring a timeline with an object argument ```tl2 = new TimeLineMax({repeat:-1});``` will set it to loop forever.
 
### Preloading with GreenSock (without pre-load)
- fade in on load
	- add ```opacity: 0``` to "myAd" style (inner container)
	- add ```tl1.to('#myAd', 0.4, {opacity: 1});``` to the beginning of your animation stack and it'll fade in before other animations play.
	
	
### Animating Individual Text
- breakup all letters into spans, give them IDs of ```id="myAd_ltr##"```.

