# My 3D scene
![scene](/images/Scene.png)
## Scene
In the context of my computers graphics module I had to create a 3D scene using openGL to show my understanding of basic rendering techniques.

I decided to make an army of nanosuits from Crysis


## Model Loading
![nanosuit](/images/Nanosuit.png)

I use assimp to load the models

I created a mesh and a model class where I put the content of the .obj for openGL to read


## Skybox
![cubemap](/images/Cubemap.png)

I used a cubemap for the skybox

Cubemaps textures can be indexed/sampled using a direction vector

It can then be used as a backgroung that seems to never move away


## Blinn-Phong
![blinn-Phong](/images/BPhong.png)

I used the Blinn-Phong model for light rendering

It consists of rendering light using 3 components : 

Diffuse, the light emited from the object

Ambient, the light from lightsources 

Specular, the portion of light reflected from the object that goes straight to the camera (the little shiny white artefact we see on eyes)

https://learnopengl.com/Lighting/Basic-Lighting


## Normal Mapping
![normalMapping](/images/NMapping.png)

Storing the normals of a mesh in a normal texture is a way of defining normals per pixel rather than by vertex, granting higher resolution to the normals

Normal maps usualy look like this

![normalMap](/images/NormalMap.png)

That's because the texture contains the xyz coordinates of the normal vector at this texcoordinates


They are stored in tangent space

I choosed to use the Tangent Bitangent Normal matrix to put the other light data in tangent space and do the light calculations in this space instead of world space

As this allows to do the matrix operation in the vertex shader instead of the fragment shader, doing as little of these operations as needed 

https://learnopengl.com/Advanced-Lighting/Normal-Mapping


## BackFace Culling
![backFaceCulling](/images/BFCulling.png)

Backface culling constists of culling every mesh face that's not facing the camera

Since each face is a triangle, openGL can check if a face is oriented towards the camera by doing a cross product with the 3 points defining the triangle

For this to work with multiple faces from multiple models, every face must be set using the same order, clockwise or counterclockwise

In openGL it only takes 3 lines of code to enable backface culling


## Model Instancing
For optimisation purposes, I instanciate the models

Instancing consists of drawing the same meshe multiple times using the same vertex data with a single draw call, it's usefull when drawing the same meshes multiple times as drawcalls are most often more costly than drawing the actual mesh.

https://learnopengl.com/Advanced-OpenGL/Instancing
