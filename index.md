# My 3D scene
![scene](/images/Scene.png)
## Scene
In the context of my computers graphics module I had to create a 3D scene using openGL to show my understanding of basic rendering techniques.

I decided to make an army of nanosuits from Crysis



## Model Loading
![nanosuit](/images/Nanosuit.png)

## Blinn-Phong
![blinn-Phong](/images/BPhong.png)

I used the Blinn-Phong model for light rendering

## Normal Mapping
![normalMapping](/images/NMapping.png)
Storing the normals of a mesh in a normal map is a way of defining normals per pixel rather than by vertex, granting higher resolution.


Normal maps usualy look like this
![normalMap](/images/NormalMap.png)




## BackFace Culling
![backFaceCulling](/images/BFCulling.png)

## Model Instancing
For optimisation purposes, I instanciate the models
The point of instancing is to draw the same meshe multiple times with a single draw call, it's usefull when drawing the same meshes multiple times as drawcalls are most often more costly than drawing the actual mesh.
This is because draw calls are sent to the GPU 
