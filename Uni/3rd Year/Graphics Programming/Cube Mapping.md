Cube maps consist of six textures representing the six faces of a cube. They are primarily used for environment mapping, where objects reflect their surroundings.

>[!info]
> In cube mapping, the texture coordinates $(s, t)$ are derived from the reflection vector, $R$, to simulate reflections on the object.

![[ExampleCubeMap.png]]
### Reflection Mapping
- Simulates reflections by applying a cube map to an object. The cube map is oriented around the object, making it appear as if the object reflects its surroundings.

### Refraction Mapping
- Uses a cube map, but simulates refraction (seeing through the object) rather than reflection.
### Skyboxes
Skyboxes are cube maps that represent distant scenery in a 3D scene, such as skies, mountains, or other far-off elements.