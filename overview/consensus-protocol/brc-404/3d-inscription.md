# 3D Inscription

Here, we delve into the attribute configurations for 3D resources. We'll take the Runestone as an example to illustrate its attribute specifications.

{% embed url="https://youtu.be/WVhYp-9SAk0" %}

## Base

<table data-header-hidden><thead><tr><th width="134"></th><th width="139"></th><th></th></tr></thead><tbody><tr><td><strong>Key</strong></td><td><strong>Required?</strong></td><td><strong>Description</strong></td></tr><tr><td>src</td><td>Yes</td><td>On-chain address of the model's source files.</td></tr><tr><td>type</td><td>Yes</td><td>Supported formats include FBX, OBJ, GLB/GLTF, STL. </td></tr><tr><td>texture src</td><td>No</td><td>Supports two types of PBR rendering workflows: metallic and specular. </td></tr><tr><td>anima src</td><td>No</td><td>Support for{}. anim format model animations and internal animations in glb format models.</td></tr></tbody></table>

## Material Texture

<table data-header-hidden><thead><tr><th width="286"></th><th width="109"></th><th width="558"></th></tr></thead><tbody><tr><td><strong>Key</strong></td><td><strong>Required?</strong></td><td><strong>Description</strong></td></tr><tr><td>Workflow mode</td><td>Yes</td><td>PBR rendering workflow, it depends on your model type. Two options: Metallic/Specular. </td></tr><tr><td>Surface type</td><td>Yes</td><td>If your model is transparent, you should select transparent option and save transparent data in alpha channel of Base Map. </td></tr><tr><td>Render Face</td><td>Yes</td><td><p>Use this to determine which sides of your geometry to render. </p><p>*Front: renders the front face of your geometry and culls the back face. </p><p>*Back: renders the front face of your geometry and culls the front face. </p><p>*Both: This is good for small, flat objects, like leaves, where you might want both sides visible.</p></td></tr><tr><td>Alpha Clipping</td><td>Yes</td><td>Makes your Material act like a Cutout Shader. </td></tr><tr><td>Base Map</td><td>No</td><td><p>Adds color to the surface, also known as the diffuse map. </p><p>*Src: On-chain address. </p><p>*Color: defalut color is white. you can use this parameter to control your model's color. e.g:(r,g,b) rgb is between 1-255.</p></td></tr><tr><td>Normal Map</td><td>No</td><td><p>With a normal map, you can add surface details like bumps, scratches and grooves. </p><p>*Src: On-chain address.</p></td></tr><tr><td>Height Map</td><td>No</td><td><p>We implement the parallax mapping technique which uses the height map to achieve surface-level occlusion effect by shifting the areas of the visible surface texture.</p><p>*Src: On-chain address. </p><p>*Intensity: the setting is a multiplier for the effect of height map. </p></td></tr><tr><td>Ambient Occlusion map</td><td>No</td><td><p>This simulates shadows from ambient light and reflection.</p><p>*Src: On-chain address.</p></td></tr><tr><td>Metalic Map/Specular Map</td><td>No</td><td><p>Shows a map input for your chosen Workflow Mode in the Surface Options. </p><p>*Src: On-chain address. </p><p>*Smoothness: Use the Smoothness slider to control the spread of highlights on the surface. It's between 0-1.</p></td></tr><tr><td>Emission Map</td><td>No</td><td><p>Makes the surface look like it emits lights.</p><p>*Src: On-chain address.</p><p>*Intensity: The intensity of self-illumination.</p><p>*Color: The color of emission. e.g:(r,g,b) rgb is between 1-255.</p></td></tr></tbody></table>

## Animation

<table data-header-hidden><thead><tr><th width="136"></th><th width="110"></th><th></th></tr></thead><tbody><tr><td><strong>Key</strong></td><td><strong>Required?</strong></td><td><strong>Description</strong></td></tr><tr><td>src</td><td>Yes</td><td>On-chain address.</td></tr><tr><td>isLoop</td><td>Yes</td><td>Choose loop option, &#x3C;0/1>.</td></tr></tbody></table>

#### Model animation supports storage in models in glb format.It also supports the mixamo public animation library, but the model must be bone-bound.

{% embed url="https://youtu.be/RfhpbP0vBdA" %}
