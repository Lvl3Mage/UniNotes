When rendering textures, you often need filtering methods to determine the color of a fragment when it doesn’t align perfectly with a texel (texture pixel). Common filtering methods include:

### 1. **Box (Nearest-Neighbor) Filtering**
   - **Description:** Uses the nearest texel’s color for the fragment.
   - **Effect:** Fast but can look pixelated up close.
>[!info]
> Box filtering is computationally simple since it only considers the closest texel, but it can produce rough-looking textures.

### 2. **Bilinear Filtering**
   - **Description:** Uses the four closest texels and interpolates between them.
   - **Effect:** Creates smoother textures than box filtering.

>[!info]
> Bilinear filtering smooths out the texture but can still appear blurry when textures are scaled up.

### 3. **Mipmapping**
   - **Description:** Uses precomputed textures at multiple resolutions in a “pyramid” to render distant objects more smoothly.
   - **Effect:** Reduces aliasing and improves performance by selecting an appropriate texture level based on distance.
   ![[Mipmapping.png]]
   ![[MipmapComparison.png]]

### 4. **Trilinear Filtering**
   - **Description:** An improvement on mipmapping that blends between levels to avoid visible transitions.
   - **Effect:** Smooths out transitions between mipmap levels, especially noticeable at mid-range distances.
   ![[Trilinear.png]]

>[!summary] **You can think of mipmapping and trilinear filtering as...**  
> choosing the “right size” texture for the job. Imagine switching to lower-resolution images the further away they are, which avoids unnecessary detail and reduces rendering workload.


![[FilteringTypes.png]]
