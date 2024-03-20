# Get Home - Unity WebGL Game
## Overview

In Get Home, players take on the role of a courageous mother duck tasked with guiding her adorable ducklings back to their coop before darkness falls. As daylight dwindles, players must navigate through the forest, strategically avoiding predators like wolves and crocodiles while utilizing special abilities to protect their ducklings. With immersive low-poly visuals and dynamic gameplay, Get Home offers a captivating journey filled with challenges and heartwarming moments.

**Game Trailer: https://youtu.be/ZRGcz-LNzS0**

**Play it here!: https://comp30019.github.io/project-2-naurway-studios/**

### Gameplay Mechanics
1. **Player Abilities** - The player will start with 3 basic abilities:
  * **Peck** - The player's basic ability. Binded to 'Q' , use this ability to fend off predators, when used in quick succession to each other and within a time frame. Knocks back the enemies.
    <p align="center">
      <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/Mother%20Duck%20and%20Duckling%20Images/peck.png" width="200"/>
      <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/newQAbility.gif" width="500"/>
    </p>
    
  * **Wing Assault** - When 'E' is pressed, the duck to rolls forwards, allowing the player to outmaneuver the enemies. However the ducklings will not follow so the player must go back and collect them.
     <p align="center">
       <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/Mother%20Duck%20and%20Duckling%20Images/wing.png" width="200"/>
       <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/abilityE1.gif" width="350"/>
       <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/abilityE2.gif" width="350"/>
       
    </p>
   
  * **Honk Surprise** - When 'W' is pressed, an egg projectile from mama duck capable of rendering an enemy stunned in surprise, opening a window of attack for mama duck.
    <p align="center">
      <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/Mother%20Duck%20and%20Duckling%20Images/honk%20.png" width="200"/>
      <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/wolfStun.gif" width="500"/>
   </p>

  * The abilities will have cooldowns - periods of time in which we cannot use these abilities. Once we use an abilitiy, the ability icon will be blacked out and message "On Cooldown!" will be displayed on screen"
  * If there is no target found for an ability, another message "Target Not Found" will be displayed on screen telling the player that the enemy is not within range to use that ability.
  <p align="center">
    <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/abilityCooldown.gif" width="400"/>
  </p>
    

2. **Dynamic placement of enemies in map**
  * Enemies are placed in the map strategically and created when the game starts. They are not static and are set to wander around a set radius. If the player enters the attack range of the enemy, they will follow the duck and attack the players ducklings. If there are ducklings, the enemies will always attack the ducklings first, if there are no ducklings left, the enemies will attack the mother duck. Once the mother duck dies, the game will end. 
  * Enemy Pathfinding: Wolves will start following when the player enters their range, and will follow them until the player exits.
    <p align="center">
      <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/enemiesUI.png" width="400"/>
    </p>
    
3. **Enemies**:
  * **Wolves, Dogs, Deers, Snakes**: These are the land predators. They attack by stalking the ducklings when they come within range, if the predators reach the ducklings, they will lunge and bite them, dealing a certain amount of damage. This continues to happen as long as the ducklings are near them. Land predators can target mama duck but will always change to a duckling if available.
    <p align="center">
     <img src = "https://github.com/edwnl/get-home-unity-game/blob/main/Images/wolf.gif" width="400"/>
    </p>

  * **Crocodiles**: These reside in the river only, they attack the duck by biting and deals damage to the duck and ducklings when they are within range.
    <p align="center">
     <img src = "https://github.com/edwnl/get-home-unity-game/blob/main/Images/crocodileGif.gif" width="400"/>
    </p>
    
  * **Boss Bear**: Appears near the end right before the duck and ducklings reach home. The bear will be able to knock up ducklings and deal more damage, it will also have more health making it harder to defeat. The bear also has the most health so it will take more damage to defeat.
    <p align="center">
     <img src = "https://github.com/edwnl/get-home-unity-game/blob/main/Images/bear.gif" width="400"/>
    </p>


4. **Battle - strategies and mechanics:**
* The player has the option to kill any predators using the available abilities but this leaves the ducklings vulnerable and at risk of losing health.
  <p align="center">
    <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/WolfDeath%2BBlood.gif" width="400"/>
  </p>
* The enemies will be able to reach and attack the last duckling in your line, tha means you will have a small window of opportunity to use your abilities to get the enemy to let go of your child. You have the option to stun them then attack or straight attack with peck in quick succession, which when done fast enough will get the enemy to let go and disengage.
  <p align="center">
    <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/wolfAttackDuckling.gif" width="375"/>
    <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/WolfAttackingDucklings.gif" width="375"/>
  </p>

* Ducklings lost to enemies will be lost permanently.
  <p align="center">
    <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/Screenshot%202023-10-31%20at%2012.51.41%20AM.png" width="400"/>
    <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/ducklingDeath.gif" width="200"/>
  </p>
  
* After every moving entity dies, they will have a death animation and a blood splatter that is from the blood particle system we used. This helps to enhance the visual effects of the game and help to emphasise the death of a character more. 

* Ducklings will only follow the mama duck if she is not too far away. If too far, the ducklings will remain stationary with a question mark around their icon.  If mama duck comes back, the question mark around their icon will disappear and the duck will follow mama duck again.
  <p align="center">
    <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/Screenshot%202023-10-31%20at%201.54.27%20AM.png" width="80" />
  </p>

* When the player gets near the boss, they will be locked in the boss arena where they must defeat the boss and obtain a key to be able to leave and get home.
  <p align="center">
    <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/main/Images/bossFight.gif" width="500"/>
  </p>
  
* During the Boss battle, the bear is able to knock up the mother duck and ducklings, introducing a new exciting challenge into the game battle.
  <p align="center">
    <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/bearKnockingUp.gif" width="400"/>
  </p>

6. Time Limit: As the limit approaches, the sun lowers leading to decreased vision. When time is up, the game will fade out to a black screen, and audio will indicate that the ducks have been overwhelmed by the predators.
   <p align="center">
     <img src = "https://github.com/edwnl/get-home-unity-game/blob/main/Images/sunrise.gif" width= "400"/>
   </p>

7. Interactive Environment: There will be water (either as a river or a pond) which will slow you down, and as wolves will not be able to pass water, will disengage them automatically. Mud puddles will slow you down if stepped on and not avoided, etc.
<p align="center">
  <img src= "https://github.com/edwnl/get-home-unity-game/blob/main/Images/duckMudShader.png" width = "450"/>
  <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/duckSwimming.gif" width="400"/>
</p>

8. Items in Game: The player will be able to pick up 2 items in game to enhance their abilities:
   * Speed Mushroom - Gain 5 second speed boost
   * Health Tomato - Health up to max health for all ducks
   <p align="center">
     <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/main/Images/powerup.png" width="300"/>
     <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/main/Images/applePowerUp.gif" width="300"/>
     <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/main/Images/mushroomPowerup.gif" width="300"/>
   </p>

  
  
## LEVELS AND WORLD DESIGN
### Game World
The game world is 3D polyart-centric where the player progresses forward through a forest at sunset. Our world is only one level but progresses through and initiates different difficulties flagged by time. The environment that our players encounter and see is largely a worn forest floor and trail which is the main path of travel, flanked on both sides by trees and bushes to create the forest environment. Elements are subject to change depending on available assets for all options. The player will occasionally encounter a river that cuts horizontally across the map and mud puddles as interference. We aim to have the player restricted to the trail. There will be an arrow near the top of the screen that will give a general idea of where the character should go in order to make it home and the game will be restricted to two axes but still rendered in a 3D environment. Below is an example created in Unity.
<p align="center">
  <img src= "https://github.com/edwnl/get-home-unity-game/blob/main/Images/world.png" alt="Image 1 Description" width = "480"/>
  <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/worldLook.png" width="480"/>
</p>

* **The Map will also feature several different areas:**
  * The area where the boss is located
    
<p align="center">
  <img src= "https://github.com/edwnl/get-home-unity-game/blob/main/Images/bearMap-wShader.png" width="500"/>
  <img src= "https://github.com/edwnl/get-home-unity-game/blob/main/Images/bearMap-v2.png" width="500"/>
</p>

  * The river, contains fish and crocodiles
  
<p align="center">
  <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/riverImage.png" width="500"/>
  <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/riverView2.png" width="500"/>
</p>

### Objects
The objects we have in the game are our enemy entities. All assets are low poly in style. When the duck collider collides with water, the duck swimming animation will activate and the movement speed of the duck slows. When the duck touches mud, the duck will also slow down but the animation will stay the same. More on interactions in the next section. 

Particles systems include fireflies and blood systems for immersion.
<p align="center">
  <img src = "https://github.com/COMP30019/project-2-naurway-studios/assets/19798018/3caa73a4-1030-4a43-9c4d-cc6f67f7ef31" width = "550"/>
</p>

The environmental physics we have are the interactions between the mud/water(river) and the player, and we aim to have their effects both visual and game-related implemented into the game (speed/slow).  Next is the interaction between the player and the enemies, all are collideable with each other. The only other interaction to note is between the ability Wing Assault where there is a knockback mechanic between the player and the wolves.

For example, when the duck enters the water, their speed will slow down and they will start swimming. 
This creates a change of pace in the game and introduces a new challenge into the game. The duck must cross the river and avoid the crocodiles under the time pressure. 
<p align="center">
 <img src = "https://github.com/edwnl/get-home-unity-game/blob/main/Images/duckswim1.gif" width="400"/>
</p>

The house will be the final destination, if the player reaches this place with the key that is only obtained after defeating the Boss, then a Victory scene will be played.
<p align="center">
  <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/home%20and%20key.gif" width="400"/>
</p>

## ART AND AUDIO
### Art Style
We aim for the art style of the game to be of a low poly style, similar to the image that is below. This style will be consistent across the game, including the forest environment, the villains and our main character and family. We aim for the colours to be vibrant in order to stay consistent with the feeling of the art style, however, base colours will look different after effects of potentially shaders for the effect of sunset and visibility. Refer below for an example created in Unity  with potential assets. 
<p align="center">
  <img src= "https://github.com/COMP30019/project-1-naurway-studios/assets/60732705/b8ba08cc-aa25-40bf-8694-411da71b3b7c" alt="Image 1 Description" width="300"/>
  <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/world.png" width="300"/>
  <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/worldLook.png" width="300"/>
</p>

**Shaders**
* We also implemented two shaders to visually enhance our map and graphics of the game.
* We implemented a 'toon-like' water shader that gives the water texture and movement making it seem like there are waves rippling through the water. The shader also gives it a toon-like look to fit into the game's style.
  <p align="center">
    <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/main/Images/waterArt.png" width="300"/>
  </p>
* We also added another celshader to enhance the colour and visuals of the map, giving it a more cartoon like look and bolder outlines. Outlines were also added through using stencil buffer operation to further enhance the toon effect and to not lose the objects inherent shape to the colours.

The current shaders that are implemented in our game, both of which are CG shaders, are: Water and Cel Shading. The two shaders were also created under the guidance and derived knowledge of tutorials to help enhance the visual aspects of our game. More on this below. 

### Shader 1: Water.shader 
Accessible [here](https://github.com/COMP30019/project-2-naurway-studios/blob/main/Assets/Shaders/Water.shader), or at Assets/Shader/Water.shader

This shader was based off of Roystan's ['Toon Water Shader'](https://roystan.net/articles/toon-water/) due to its toon-like approach to fit into the game's style. This tutorial was easy to follow and helped in deepening shader understanding alongside what was learnt alongside this course. There were concepts learnt in workshops that were applied in very creative ways which I will get into. 
<p align="center">
  <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/main/Images/waterArt.png" width="400"/>
</p>

This shader functions create visual effects and water colour through calculating the water depth - relative to the camera's view - and then uses this information to creatively render the 'shoreline' foam of water. Noise and distortion textures were then used to create the surface waves. Lastly, actual wave movements were added through the vertex shader using sin through the x and y planes to create a dynamic and animated water surface. 
<p align="center">
  <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/main/Images/riverGif.gif" width="400"/>
  <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/main/Images/duckswim1.gif" width="400"/>
</p>
<p align="center">
  Here we have the river in game with the waves flowing and the water shader
</p>

<p align="center">
  <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/main/Images/riverView2.png" width="400"/>
  <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/main/Images/duckSwimming.gif" width="400"/>
</p>

**Properties**: 
The shader defines a set of properties for colours, textures and more appearance control related variables for customization. The vertex shader, besides transforming object vertices into clip space, handles wave movement which as mentioned before was through the manipulation of x and y axis with sin. This was controlled by the _Frequency and _Amplitude properties and helped create the effect of lapping 'waves' on the shores. 

```
Properties
    {	
        _Shallow("Depth Gradient Shallow", Color) = (0.325, 0.807, 0.971, 0.725)
        _Deep ("Depth Gradient Deep", Color) = (0.086, 0.407, 1, 0.749)
        ...
        _Frequency("Frequency", Range(0, 200)) = 100
        _Amplitude("Amplitude", Range(0, 2)) = 1
        
    }   

```
The 'Properties' block defines the shader's editable parameters that can be changed within the Unity editor to customise the appearance of water.

**SubShader**: The SubShader block describes how the shader should be rendered by the graphics pipeline. 
* We set it to render in the transparent queue with forward base light mode, which means it will be drawn after opaque objects and will interact with directional light sources.
* It uses blending to ensure transparency is handled correctly, and it does not write to the Z-buffer (ZWrite Off), which is typical for transparent objects to avoid depth conflicts.
* The 'Pass' block block contains the programmable GPU code that defines exactly how the pixels and vertices will be rendered:
  * alphaBlend: A custom blending function for combining the foam and water colors.
  * Vertex and fragment shader functions (vert and frag) for calculating the vertex positions and the final colour for each pixel.

```
SubShader
    {
        Tags {
            "RenderType"="Transparent" 
            "Queue"="Transparent"
            "LightMode" = "ForwardBase"
	          "PassFlags" = "OnlyDirectional"
        }
        Pass
        {

            #include "UnityCG.cginc"
            float4 alphaBlend(float4 top, float4 bottom) {
               ...
            }

            v2f vert (appdata v)
            {
              ...
            }

            float4 frag (v2f i) : SV_Target
            {
               ...
            }
        }
    }

```
The fragment shader calculates the depth of each pixel relative to the camera and relative to the surface of the water. Colours were then interpolated between the _Shallow colour and _Deep colour to form the water. _CameraDepthTexture was the depth map obtained and used for this. Additional movements were introduced via a distortion texture where the red and green channels were used to pull the noise texture to create dynamics and flow. 

**Shader Functionality**
* When the shader is applied to a mesh, it will render the mesh with a water-like appearance.
* The colors will change from shallow to deep based on the distance from the surface, simulating how water appears in real life.
* The noise texture adds variation to the surface, making it look more like water rather than a flat surface.
* The foam is created based on the depth and the noise texture, giving the impression of waves and froth.
* The distortion texture is scrolled over time to create the illusion of moving water.
  <p align="center">
    <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/main/Images/waterComponent.png" width="500"/>
  </p>



<br></br>
### Shader 2: CelShading.shader
Accessible [here](https://github.com/COMP30019/project-2-naurway-studios/blob/main/Assets/Shaders/CelShading.shader), or at Assets/Shader/CelShading.shader

This shader was a blend of knowledge learnt from both Roytoon's ['Toon Shader'](https://roystan.net/articles/toon-shader/)  and Daniel Iletts ['Cel Shading Introduction'](https://danielilett.com/2019-05-29-tut2-intro/) to create the desired effect. Outlines were also added through using stencil buffer operation to further enhance the toon effect and to not lose the objects inherent shape to the colours. This was the shader that created the biggest different visually to the game based on toon/cel shading concepts.

<p align="center">
  <img src = "https://github.com/COMP30019/project-2-naurway-studios/blob/main/Images/world.png" width= "400"/>
  <img src = "https://github.com/COMP30019/project-2-naurway-studios/blob/main/Images/worldLook.png" width="400"/>
</p>

The properties defined handle the customizable properties of the shader, including specular reflections, rim lighting and colours for each. There are also properties for antialiasing, intensities and outlines. This shader also contains two pass's, one for the main rendering and one to render the outlines. The first pass does the transformation of object vertices to clip space, shadow coordinates transfer, calculations of normals and uv coordinates to transfer various parameters to the fragment shader. The lighting model used to calculate diffuse lighting is Lambertian lighting (lighting point on a surface is based on the angle between light source and normal vector, calculated by the dot product). Shadows are included through the use of SHADOW_ATTENUATION(i). 

```
// Lambertian Lighting
  float3 normal = normalize(i.worldNormal);
  float diffuse = dot(_WorldSpaceLightPos0, normal);
```

Specular lighting here is based on the Blinn-Phong model and calculates the specular intensity based on the dot product between the half vector (vector halfway between view and light direction) and the normal vector. It's then modified based on _Glossiness which was multiplied twice to have a larger effect. The rim lighting (light around the edges of an object) was then created from the inverse of the dot product between view direction and normal vector. 

```
// Blinn-Phong Lighting
float3 halfVec = normalize(_WorldSpaceLightPos0 + viewDir);
float lightDotP = dot(normal, halfVec);
float specularIntensity = pow(lightDotP * diffuseSmooth, _Glossiness * _Glossiness);
```
There was an alteration made to transfer shadow coordinates since TRANSFER_SHADOW() wasnt initalizing properly, to which a fix was found from [this forum](https://forum.unity.com/threads/shader-warning-with-no-reason.1103143/) thread. 

Lastly, the second pass focused on rendering the outline which was achieved through stencil testing taught by Daniel Iletts tutorial as linked above. Objects are rendered with a specific stencil ID then rendered again with a different stencil comparison in order to create the outline effect. The different stencil ID ensured lines are able to be seen over different materials.
In the vert function, it inflates the object's vertices along their normals by the _OutlineSize, and the frag function simply outputs the _OutlineColor.
```
 Pass {

    Stencil {
	Ref [_ID]
	Comp notequal
	Fail keep
	Pass replace
    }
    ...
    v2f vert(appdata v) {
	v2f o;
	float3 normal = normalize(v.normal) * _OutlineSize;
	float3 position = v.vertex + normal;

	o.vertex = UnityObjectToClipPos(position);

	return o;
    }     
}

```
<p align="center">
  <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/main/Images/celShaderComponent.png" width="400"/>
</p>
<p align="center">
The celShader was added to every object as a material
</p>


Here are some examples of the shader working in gameplay: 
<p align="center">
  <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/main/Images/wolfStun.gif" width="400"/>
  <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/main/Images/bearMap-wShader.png" width="400"/>
  <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/main/Images/newQAbility.gif" width="400"/>
  <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/main/Images/Screenshot%202023-10-31%20at%2010.41.48%20PM.png" width="400"/>
</p>
  
<br></br>
<br></br>
### Particle Systems

We have used two particle systems to enhance visual effects in our game. 
One is a Firefly Particle System and the other is a Blood VFX Particle System.

#### FireFly Particle System
<p align="center">
  <img src = "https://github.com/COMP30019/project-2-naurway-studios/blob/README_Drafts/Images/fireflies.gif" />
</p>
<p align="center">
  <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/README_Drafts/Images/Screenshot%202023-10-28%20at%2011.31.27%20AM.png" width="300"/>
  <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/README_Drafts/Images/Screenshot%202023-10-28%20at%2011.31.05%20AM.png" width = "300" />
</p>
The Firefly Particle System is one of the two particle systems employed to elevate the visual effects in our game. It is designed to create a realistic firefly effect, enhancing the immersive and atmospheric elements of the game environment. 
Randomness was utilised in the Firefly Particle System using the Noise attribute. This allowed the particles to move in random directions, contributing to a more realistic effect.
<p align="center">
  <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/README_Drafts/Images/Screenshot%202023-10-28%20at%2011.29.07%20AM.png" width = "600"/>
</p>

  **Attributes Varied**
  - Start size set to small to mimic the size of real fireflies.
  - Start speed is 0 becaseu fireflies don't start moving immediately.
  - Emission = 20, to create a significant number of fireflies
  - Shape = Sphere, allows fireflies to disperse in all directions
  - Radius = 10, give the fireflies wide area to move in
  - Colour over lifetime = yellow to mimic the glow of real fireflies.
    <p align="center"> 
      <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/README_Drafts/Images/Screenshot%202023-10-28%20at%2011.50.33%20AM.png" width = "300"/>
    </p>
  - Size over lifetime attribute was set to give the effect of fireflies twinkling in the distance
  - Noise was applied to have particles move in random directions, imitating the erratic flight pattern of fireflies. The strength was decreased to give the particles a slow, softer effect, again mirroring real fireflies. The frequency was also adjusted to further enhance this effect.
    
      <p align="center">
        <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/README_Drafts/Images/Screenshot%202023-10-28%20at%2011.42.17%20AM.png" width = "300" />
        <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/README_Drafts/Images/Screenshot%202023-10-28%20at%2011.47.41%20AM.png" width = "300"/>
        <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/README_Drafts/Images/Screenshot%202023-10-28%20at%2011.48.50%20AM.png" width = "300"/>
    </p>


#### Blood VFX Particle System Using Shader Graph 
The Blood VFX Particle System is the second particle system used in our game to create visually striking effects. Specifically designed using custom a Shader Graph and Material to simulate the appearance of blood in a realistic and engaging manner.
<p align="center">
  <img src = "https://github.com/COMP30019/project-2-naurway-studios/blob/README_Drafts/Images/blood%20clip.gif" />
</p>

<p align="center">
  <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/README_Drafts/Images/Screenshot%202023-10-28%20at%2011.55.49%20AM.png" width="300"/>
  <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/README_Drafts/Images/Screenshot%202023-10-28%20at%2011.55.57%20AM.png" width = "300" />
</p>


##### Blood VFX Shader Graph 
The Shader Graph was used to create custom shaders for the Blood VFX Particle System. This provided the flexibility to design the visual effects with precise control over how the particles look and behave. Using Shader Graph, we could procedurally generate a realistic-looking blood texture, add movement to the particles, adjust the thickness and contrast of the blood, and create a more volumetric look by adding a normal map.

Randomness was utilized in several ways including the start lifetime, size, and start rotation of the particles to create a more realistic and varied blood effect.
The rationale for these choices was to create a blood effect that is visually striking, realistic, and enhances the overall aesthetic of the game. The blood effect was also designed to perform well and not overload the game as the number of enemies increases.

<p align="center">
  <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/README_Drafts/Images/Screenshot%202023-10-28%20at%2012.21.12%20PM.png" width="800"/>
</p>
<p align="center">Full Shader Graph - The Nodes on the left before the blue nodes are part of the procedurally generated Blood VFX</p>

<p align="center">
  <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/README_Drafts/Images/Screenshot%202023-10-28%20at%2012.18.10%20PM.png" width="150" height = "300"/>
  <img src="https://github.com/COMP30019/project-2-naurway-studios/blob/README_Drafts/Images/Screenshot%202023-10-28%20at%2012.31.10%20PM.png" width="150" height = "300"/>
</p>
<p align="center">Shader Graph Attributes</p>

  **Explanation**
  1. In the master node we first added base, emission and specular colouring. 
  2. Added simple noise, scaled to 40, this makes our texture become transparent in places of black spots
  3.  Then we added mask, we added texture2D, using the default unity particle texture, and connected it to Sample texture 2D, added it to a multiply node, so that we can subtract our mask from our noise
  4.  Smoothness 0, so it becomes darker.
  5. Tiling and offset connected to UV of simple noise. To make the particles move at the speed we want, we controlled the speed by adding in a Float called Speed.
  6. We multiply the time by our speed and connect the result of the multiplication to the tiling and Offset nodes Offset.
  7. Next we added a second layer of noise, with scale 100 so it is more granular, multiply that with our original simple noise with the more granular simple noise. And connected that multiplication with the other multiplication that is multiplying our Mask.
  8. Next we added more movement to our particles, we did so by adding a Tiling and Offset node to our more granular noise, connect it to the UV of the granular noise. We want to make it move in the opposite direction, so we multiply it by the result of the multiplication of time by speed by -1 and connect it to the Offset of the second Tiling and Offset node
  9. Next, the blood looks a bit thin, so we want to increase the thickness. To do this, we multiplied our noise pattern by 2, so that it becomes brighter. Then we increased the contrast by 3, and then connect our new multiplication with the Mask.
  10. Next, to make it more volumetric, we add a normal map. We do this by adding a node called Normal from Height. From our procedurally generated Blood texture we connect to the normal from height node, then we add a normal strength node with a value of 4, and connect to Normal of the master node.

<p align= "center">
  <img src = "https://github.com/COMP30019/project-2-naurway-studios/blob/README_Drafts/Images/blood.gif"/>
</p>


**Blood Particle System Varied Attributes**
1. Duration = 1.5, allows the blood effect to persist 
2. Randomise Start Lifetime between two constants 4 and 7 to create variation in the lifetime of the blood particles
3. Size of blood particles randomised with values between 2 and 2.2 to give more textured and realistic appearance.
4. Start rotation randomly set between 0 and 360 degrees for more dynamic and less uniform blood effect
5. Gravity modifier = 2, mimics effect of gravity on blood.
6. Start Speed = 0.5
7. Shape = Sphere, allows blood particles to disperse in all directions for a more dramatic effect.

**Blood Particle Instantiation**
When enemies or ducklings die, the blood particle system game oject will be instantiated. 
```
LivingEntity,cs Script
//For blood on death
public GameObject Blood; // New attribute 


public virtual void Die()
{
    Destroy(gameObject);

    if (Blood is not null)
    {
        Instantiate(Blood, transform.position, Quaternion.identity);
    
    }
 
}
```

The script for destroying blood effects helps maintain optimal game performance by removing instances of the blood particle system, preventing the game from becoming burdened over time. This is particularly important as the quantity of enemies, and therefore blood effects, increases during gameplay.

```

public class BloodDestroyer : MonoBehaviour
{

    // Update is called once per frame
    void Update()
    {
        Destroy(gameObject, 0.5f); // after 0.5f the instantiation of the Blood game obejct will be destroyed
    }
}
```
  
### Sound and Music
We aim for something akin and inspired by Doki Doki Literature Club, quiet background music with environmental noises such as trees rustling and wind blowing. We aim to have sound cues for when difficulty increases in the set minute intervals (i.e: wolves howling) and a falcon screech when the alert for falcon incoming is on screen. 
* Resources: https://mixkit.co/free-sound-effects/game/, https://www.sounds-resource.com/, https://www.zapsplat.com/sound-effect-category/game-sounds/, SoundCloud,

Music Used: 
* Main menu and instructions background music
  * https://www.youtube.com/watch?v=HSLwh_KOVBk
* While playing the game
  * https://www.youtube.com/watch?v=7cxYeiNutbs
* For Boss Fight
  * https://www.youtube.com/watch?v=X_ME_LndEi4
* For victory after defeating the boss
  * https://www.youtube.com/watch?v=TUqvYZn5nvc
* For the Victory Scene
  * https://www.youtube.com/watch?v=5pSCjNkHaOU
* Game over scene
  * https://www.youtube.com/watch?v=amAqGQ1vN6E

Sounds used: 
* Duck quack
* Bird wings flapping
* Wolves howling
* Forest sounds
* Sounds in PolyPerfect assets

## USER INTERFACE (UI)
The game’s UI is simple, we want everything to have a soft, round feel to it. We have attached an example for the sample UI for the game. The aesthetic should feel in line with the game’s poly art cute style, however have colours that are slightly less saturated compared to the game’s palette to draw less attention away from the main game. A menu can potentially be added for rebinding of keys as an extension. 
<p align="center">
  <img src="https://github.com/COMP30019/project-1-naurway-studios/assets/60732705/ebcb5335-e60b-4986-a505-41cb21228c99" alt="Image 1 Description" width = "450"/>
  <img src = "https://github.com/edwnl/get-home-unity-game/blob/main/Images/newUIwShader.png" width = "500" />
</p>

**Health UI**
* Every moving entity (excluding Fish) will have a health bar above it. This indicates the percentage of health left before the moving entity is dead.
* The colour of the health UI distinguishes which entity it is:
  * Yellow - Mother Duck
  * Green - Ducklings, when the ducklings are very low health and are about to die, the UI health bar will turn red.
  * Red - Enemies.
  <p align="center">
    <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/healthUIDuck.png" width="300"/>
    <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/healthUIRed.png" width="300"/>
    <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/Screenshot%202023-10-31%20at%201.59.29%20PM.png" width="300"/>
  </p>


**Game Over Screen**
* This screen is shown when either the 5 minute timer runs out and the player is not home yet
* Or when the player has lost all 5 of their ducklings and the enemy predators have killed the mother duck. 
  <p align="center">
    <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/Screenshot%202023-10-31%20at%202.17.05%20AM.png" width="400"/>
  </p>

**Victory Screen**
* This screen is shown when the player has successfully reached the house with the key after defeating the boss.
  <p align="center">
    <img src="https://github.com/edwnl/get-home-unity-game/blob/main/Images/Screenshot%202023-10-31%20at%202.18.15%20AM.png" width="400"/>
  </p>

**Main Menu Screen**
* This will be the first screen that the player will see
* It will have instructions and a description of the enemies and items
  <p align="center">
    <img src = "https://github.com/edwnl/get-home-unity-game/blob/main/Images/Screenshot%202023-10-31%20at%207.45.24%20PM.png" width="500"/>
    <img src = "https://github.com/edwnl/get-home-unity-game/blob/main/Images/Screenshot%202023-10-31%20at%207.46.01%20PM.png" width="500"/>
    <img src = "https://github.com/edwnl/get-home-unity-game/blob/main/Images/Screenshot%202023-10-31%20at%207.46.07%20PM.png" width="500"/>
  </p>
  
## TECHNOLOGY AND TOOLS
Following list of software and tools we intend to use for this project:
* Github
* Unity
* Discord (for communication)
* Trello (to track feature implementations)
* Ableton Live & Audacity (Creating and modifying game audio)
* Blender (3D modelling)
* Clip Studio Paint/Procreate (Creating cutscenes)
* Photoshop (Image editing for UI, etc.)
* Premiere Pro (creating & editing the game trailer)
* Jetbrains Rider / Visual Studio Code (code editing)

<p align="center">
 <img src = "https://github.com/COMP30019/project-2-naurway-studios/assets/19798018/079c659e-33f3-4221-897e-5323276d7a2e" width="300"/>
 <img src = "https://github.com/COMP30019/project-2-naurway-studios/assets/19798018/f500b4bf-c89b-4e2c-8c3d-dbd6e6d69a86" width="350"/>
</p>
 
<p align="center">
  <img src = "https://github.com/COMP30019/project-2-naurway-studios/assets/19798018/d1a20921-c1d9-4232-b8bb-fab6e330025a" width = "800" />
</p>
Here we have used the website Trello to create a board for our Project. This is convenient as it allows us to create lists and cards to track tasks and subtasks. Each team member is able to assign tasks, set due dates, and track project progress. 
Also having each part of the project laid out in a board like view helps to visualise the workflow and progress of the project. 
