#Instancing

###Rationale

Having a scene and throwing nodes to it might work for small projects, but as a project grows, more and more nodes are used and it can quickly become unmanageable. To solve this, Godot allows a project to be separated in several scenes. This, however, does not work the same way as in other game engines. In fact, it's quite different, So please do not skip this tutorial!

To recap: A scene is a collection of nodes organized as a tree, where they can have only one single node as the tree root. 

<p align="center"><img src="images/tree.png"/></p>

In Godot, a scene can be created and saved it to disk. As many scenes can be created and saved as desired.

<p align="center"><img src="images/instancingpre.png"/></p>

Afterwards, while editing an existing or a new scene, other scenes can be instanced as part of it:

<p align="center"><img src="images/instancing.png"/></p>

In the above picture, Scene B was added to Scene A as an instance. It may seem weird at first, but at the end of this tutorial it will make complete sense!

###Instancing, Step by Step

To learn how to do instancing, let's start with downloading a [pre-made scene](media/instancing.zip).

Unzip this scene in any place of our preference. Then, add this scene to the project manager using the 'Import' option:

<p align="center"><img src="images/importproject.png"/></p>

Simply browse to inside the project location and open the "engine.cfg" file. The new project will appear on the list of projects. Edit the project by using the 'Edit' option.

This project contains two scenes "ball.scn" and "container.scn". The ball scene is just a ball with physics, while container scene has a nicely shaped collision, so balls can be thrown in there.

<p align="center"><img src="images/ballscene.png"></p>
<p align="center"><img src="images/contscene.png"/></p>

Open the container scene, then select the root node:

<p align="center"><img src="images/controot.png"/></p>

Afterwards, push the '+' shaped button, this is the instancing button!

<p align="center"><img src="images/continst.png"/></p>

Select the ball scene (ball.scn), the ball should appear in the origin (0,0), move it to around the center
of the scene, like this:

<p align="center"><img src="images/continstanced.png"/></p>

Press Play and Voila! 

<p align="center"><img src="images/playinst.png"/></p>

The instanced ball fell to the bottom of the pit. 

###A Little More

There can be as many instances as desired in a scene, just try instancing more balls, or duplicating them (ctrl-D or duplicate button):

<p align="center"><img src="images/instmany.png"/></p>

Then try running the scene again:

<p align="center"><img src="images/instmanyrun.png"/></p>

Cool, huh? This is how instancing works.

###Editing Instances

Select one of the many copies of the balls and go to the property editor. Let's make it bounce a lot more, so look for the bounce parameter and set it to 1.0:

<p align="center"><img src="images/instedit.png"/></p>

The next it will happen is that a green "revert" button appears. When this button is present, it means we modified a property from the instanced scene to override for a specific value in this instance. Even if that property is modified in the original scene, the custom value will always overwrite it. Pressing the revert button will restore the property to the original value that came from the scene.

###Conclusion

Instancing seems handy, but there is more to it than it meets the eye! The next part of the instancing tutorial should cover the rest..


