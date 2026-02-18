<h1>Ragdoll Revival</h1>

<p align="center"><img src="Images/MainScreen.png" alt="Main Screen View" height=360 width=640/></p>
<p align="center">A game-jam game made for Godot Wild Jam #74</p>

<h3>Summary</h3>
<p>&emsp;You find yourself in an old, abandoned attic. There appears to be a doll present; beaten and broken. You feel compelled to repair it.</p>

<h3>Where To Play?</h3>
<p>&emsp;You can play this game directly in your browser either via the <a href=https://doctorsquawk.itch.io/ragdoll-revival>itch.io page</a> or here on <a href=https://jbevell.github.io/Ragdoll-Revival/>github pages</a>.</p>

<h3>Game Controls</h3>
<p>&emsp;This is a point-and-click style game controlled entirely with a mouse. Click on inventory items on the left side of the screen and use them to interact with elements in the game. You may click a selected inventory item again to deselect it.</p>

<h3>Development Notes</h3>
<h4><i>About the Jam</i></h4>
<p>&emsp;Godot Wild Jam #74 took place on October 11, 2024. The main theme was "Haunted", with three optional themes or design elements called "Wildcards". I opted to use the Wildcard "It's Broken - The player needs to repair and/or restore something". All participants had until October 20, 2024 to design, develop, test, and publish their submissions.</p>

<h4><i>Game Design Overview</i></h4>
<p>&emsp;It's Halloween! Or, close enough. As a fan of horror, I was excited to participate and play other participants' submissions for this jam. I had also been wanting to try my hand at a point-and-click style game, having just played the entire Myst series. Trying my hand at the basics seemed like a good idea during a jam. The idea for this one came quickly once I saw the Wildcards. What I ended up creating for the scene was essentially what I had seen in my head except for the doll's design. She was originally going to be much more ambiguous in style but I liked the idea of making a nod to the Sadako hair-over-the-face look.</p>
<p>&emsp;The room came together through trial and error, considering what could create plausible interactions for the player to figure out, a little bit of just making decisions and hoping that they worked, and an attempt to prevent the possible interactions from getting too large in scope. I ended up drawing a flow chart of the object interactions, specifically to ensure that I wouldn't accidentally create extra complexity.</p>

<p align="center">
<img src="Images/RoomSketch.png" alt="Room Sketch" height=300 width=300/>
&emsp;
<img src="Images/ItemInteractionTree.png" alt="Item Interaction Tree" height=300 width=300/>
</p>

<h4><i>Programming and Development</i></h4>
<p>&emsp;The two major parts that I wanted to work on during this project were the implementation of an inventory system and the control of the flow of interaction between the inventory items and the environment. The items in the scene, which I called "interactive objects", were fairly easy to implement. I created a parent script that handled the basic interactivity of these objects. Then, I made child scripts for each of the individual objects that extended this parent. The children mostly contain definitions for signals that print the appropriate text for the state of the game during an interaction attempt. In hindsight, there's most likely a way to reduce the scripts even further and only change a few variables.</p>
<p>&emsp;The inventory took me a long time to do and I still want to start over on it. It was split between two main scripts, the inventory and individual inventory spaces. Spaces stored the data on what object they held and handled displaying their own selection highlights. But the inventory script handled everything else. It was way too much to put onto one script and the signals between the inventory and the spaces became some terrible spaghetti for me. This was with an extra week after the jam trying to untangle the mess. For all of the trouble it gave me, it does seem to work properly. I think starting over someday with some proper planning would lead to better results.</p>
