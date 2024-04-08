# 3D Inscription

Here, we delve into the attribute configurations for 3D resources. We'll take the Runestone as an example to illustrate its attribute specifications.

{% embed url="https://youtu.be/WVhYp-9SAk0" %}

## Base

<table data-header-hidden><thead><tr><th width="134"></th><th width="139"></th><th></th></tr></thead><tbody><tr><td><strong>Key</strong></td><td><strong>Required?</strong></td><td><strong>Description</strong></td></tr><tr><td>src</td><td>Yes</td><td>On-chain address of the model's source files.</td></tr><tr><td>type</td><td>Yes</td><td>Supported formats include FBX, OBJ, GLB/GLTF, STL.</td></tr><tr><td>texture src</td><td>No</td><td>Supports two types of PBR rendering workflows: metallic and specular.</td></tr><tr><td>anima src</td><td>No</td><td>Support for{} .anim format model animations and internal animations in glb format models.</td></tr></tbody></table>

## Material Texture

<table data-header-hidden><thead><tr><th width="266"></th><th width="138"></th><th></th></tr></thead><tbody><tr><td><strong>Key</strong></td><td><strong>Required?</strong></td><td><strong>Description</strong></td></tr><tr><td>Workflow mode</td><td>Yes</td><td>metallic /specular</td></tr><tr><td>Surface type</td><td>Yes</td><td>Opaque/Transparent</td></tr><tr><td>Render Face</td><td>Yes</td><td>Front,Both,Back.</td></tr><tr><td>Alpha Clipping</td><td>Yes</td><td>-</td></tr><tr><td>Base Map</td><td>No</td><td>If needed, provide src+color.</td></tr><tr><td>Normal Map</td><td>No</td><td>If needed, provide src.</td></tr><tr><td>Height Map</td><td>No</td><td>If needed, provide src+Intensity.</td></tr><tr><td>Ambient Occlusion map</td><td>No</td><td>If needed, provide src.</td></tr><tr><td>Metalic Map/Specular Map</td><td>No</td><td>If needed, provide src+Intensity+Smoothness .</td></tr><tr><td>Emission Map</td><td>No</td><td>If needed, provide src+Color+Intensity.</td></tr></tbody></table>

## Animation

<table data-header-hidden><thead><tr><th width="136"></th><th width="110"></th><th></th></tr></thead><tbody><tr><td><strong>Key</strong></td><td><strong>Required?</strong></td><td><strong>Description</strong></td></tr><tr><td>src</td><td>Yes</td><td>On-chain address of the model's source files.</td></tr><tr><td>isLoop</td><td>Yes</td><td>Choose loop option, &#x3C;0/1>.</td></tr></tbody></table>

{% embed url="https://youtu.be/RfhpbP0vBdA" %}
