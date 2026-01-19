## What?
During my deep dive I want to create a shader that give a pixel art look to 3D games. This shader then can be used by other students or developers to make 3D models look like pixel art. I got the inspiration for the project from the popular game Dead Cells, but since then the technique is more wide spread and used by many different games. 
During the development of Dead Cells Thomas Vasseur was the only artist in the team for a year. To be able to design animations and models fast for the game they created a program to transform 3D models and animations into 2D pixel art. This sped up the creation of art assets that one person could create and still fit the style of the game. The pipeline converts  the model into 2D by using shaders and compressing the size of the model. I will also look at other games that use the model of working and see how they did it. I want to recreate the shaders that are used for the transformation process. I will use Unity the demonstrations.

## Why?
Creating art for any game is time consuming and usually small teams and solo developers have too much to do. Firstly if you game is in a pixel art art style it is very labor intensive to create animations because each frame has to be drawn by hand. Compared to this creating models and especially animations in 3D is a lot faster and easier. As we can see looking at Dead Cells the process speeds up asset creation a lot even if there is one artist in the team. Also I have been interested in shaders for a long time and I think this topic can be a great introduction on how they work and how to use them in Unity.

## How?
I want to recreate the pixel art look with shaders in Unity. I am considering to create a shader for the full screen and for individual models.
Questions:
How does the pipeline work? What steps does it take to convert assets?
What kind of shaders do they use in the pipeline?
What are the limitations of the process?

I will recreate the shaders in Unity with the shader graph tool. I want to have a demo with the shaders on and without the shaders to compare on a 3D model. 

## Use
### Phase 1: Create the Material
Shader Graphs cannot be assigned directly to the renderer; they must be wrapped in a Material.

-In your Project window, right-click on your shader graph file.

  - Select Create > Material.

  - Name it something like Mat_PixelArt.

### Phase 2: Add the Render Feature
Since this is a fullscreen effect, you don't drag it onto an object in the scene. You add it to the graphics pipeline itself.

Apply shader to renderer:

- Go to Assets > Settings and open the PC_Renderer asset.

- In the inspector go to Full Screen Pass Renderer Feature.

- Set the Pass Material to you newly created material (Mat_PixelArt).

### Phase 3: Set Camera to Orthographic
To achieve a pixel art 2D look you have to set the camera to Ortographic view.

Select your Main Camera in the Hierarchy.

- In the Inspector, find the Camera component.

  - Change Projection from Perspective to Orthographic.

### Phase 4: Configure the Parameters
- Select your Mat_PixelArt material.

- In the Inspector, you need to set values for the properties you exposed:

- Pixel Resolution: Try 320 or 480 (This sets the vertical pixel count). Make sure the selected number is a multiple of 4, if not the pixels will be different sizes.

- Color Count: Try 16 or 32. (If this is 0 or 1, your screen might turn black or solid white).

- Dither Pattern: For me the best results were between 0-1. Try a couple and see which number you like.


There are also other tools that can be considered for pixelizing models that are more like the tool developed by Motion Twin:

Pro Pixelizer: https://propixelizer.github.io/docs/usage/pixelization/

Pixelover: https://docs.pixelover.io/manual/introduction/
