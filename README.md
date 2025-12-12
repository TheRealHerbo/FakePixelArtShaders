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


## Outcomes
### Shader graph

<img width="2116" height="658" alt="Screenshot From 2025-12-10 20-39-28" src="https://github.com/user-attachments/assets/7e82d89d-9d93-4833-b1dc-61b03c39b70d" />

### How it looks on models:
<img width="2862" height="1510" alt="Screenshot From 2025-12-10 20-37-03" src="https://github.com/user-attachments/assets/f884b0e7-bd5d-4482-af0f-2a87adef317e" />
