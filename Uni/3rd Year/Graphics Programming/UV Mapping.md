## Texture Coordinates (UV Mapping)

### Definition
Texture coordinates ($s, t$) map points on a texture image to points on a 3D model. They range from $[0, 1]$ on both axes, defining how the texture wraps around the object.

>[!info]
> Texture coordinates are assigned to each vertex on the 3D model. By mapping these coordinates to specific points on a texture image, the model can display the image in a way that fits its geometry.

>[!summary] **Intuition for Texture Coordinates**  
> Imagine laying a grid (the texture space) over a photo. Each point on this grid, defined by $(s, t)$ values, is then applied to specific points on your 3D model. Think of it as “wrapping” the texture around the model like gift wrap.


![[Texcoords.png]]

---

## Repeating Textures

Textures can repeat over a surface by using $s$ and $t$ values greater than 1.

>[!info]
> When texture coordinates exceed $1$, the integer part is discarded, allowing the texture to “tile” over the surface continuously.

>[!summary] **Intuitive Explanation for Texture Tiling**  
> If you imagine the texture as a wallpaper pattern, repeating the texture simply “tiles” the pattern across the surface. Coordinates over 1.0 help “wrap” the wallpaper multiple times over a large surface area.
 
