## Phong Illumination Model

The Phong illumination model combines three core components—ambient, diffuse, and specular reflection—to create a realistic lighting effect on surfaces.

>[!summary] **Understanding Phong Model**  
> Think of the Phong model as layering different "types" of light on top of each other to approximate how light behaves in the real world. Ambient light fills in the shadows with a base layer of light. Diffuse reflection makes surfaces visible from any angle, as it spreads light evenly. Finally, specular reflection adds shiny highlights where light reflects at sharper angles toward the viewer.

### 1. **Ambient Illumination**
- **Definition:** Uniform, background illumination across the scene, simulating indirect light from the environment.

>[!info]
> $$ I_a = k_a \cdot L_a $$  
> Where $I_a$ is ambient intensity, $k_a$ is the ambient reflection coefficient, and $L_a$ is the ambient light intensity.

>[!summary] **You can think of ambient light as...**  
> a base level of light that fills the scene uniformly, ensuring that no part of the object is entirely in shadow. Imagine it as the "room light" that keeps everything visible even if there’s no direct light source shining on it.  

### 2. **Diffuse Reflection (Lambertian Reflection)**
- **Definition:** Light is scattered in all directions from a surface, as if the surface were "matt" or non-shiny. Based on Lambert's Cosine Law, which states that perceived intensity is proportional to the cosine of the angle $\theta$ between the light direction and the normal.

>[!info]
> $$ I_d = k_d \cdot L_d \cdot \cos(\theta) = k_d \cdot L_d \cdot (L \cdot N) $$  
> Where $k_d$ is the diffuse reflection coefficient, $L_d$ is the diffuse light intensity, $L$ is the light vector, and $N$ is the normal vector at the point.

>[!summary] **Think of diffuse reflection as...**  
> spreading light evenly across the surface. It’s what lets us see the object’s color and shape regardless of the viewing angle. The amount of light depends on the angle between the light source and the surface—direct light (perpendicular) appears brightest.

### 3. **Specular Reflection**
- **Definition:** Adds bright highlights to shiny surfaces, where light reflects at a particular angle towards the viewer.

>[!info]
> $$ I_s = k_s \cdot L_s \cdot (R \cdot V)^{\alpha} $$  
> Where $k_s$ is the specular reflection coefficient, $L_s$ is the specular light intensity, $R$ is the reflection vector, $V$ is the view vector, and $\alpha$ (shininess) determines the sharpness of the specular highlight.

>[!summary] **Intuition for Specular Reflection**  
> You can think of specular reflection as the "shine" or "glare" you see on a polished surface. It’s strongest when the light bounces directly toward you. The $\alpha$ value (shininess) controls how sharp or broad this highlight is—low values make it broad (like plastic), and high values make it sharp (like metal).

### Combined Illumination
- **Total Illumination:** The combined effect of ambient, diffuse, and specular light.

>[!info]
> $$ I = I_a + I_d + I_s $$

---

## Shading Models

Shading determines how the illumination model is applied across the surface.

### 1. **Flat Shading**
- **Process:** Illumination is calculated once per polygon using the polygon's normal vector.
- **Effect:** Gives a faceted, blocky look, suitable for low-detail surfaces.

>[!summary] **Understanding Flat Shading**  
> In flat shading, think of each polygon as a "tile" that reflects light uniformly. This results in sharp, visible edges between polygons, making it best for large, flat surfaces.

### 2. **Gouraud Shading**
- **Process:** Illumination is calculated at each vertex, and the colors are interpolated across the surface.
- **Effect:** Smooth transitions between vertices, though it may not capture specular highlights accurately on larger polygons.

>[!summary] **You can think of Gouraud shading as...**  
> calculating colors at the "corner points" (vertices) and then blending them across the polygon’s face. It’s a more efficient method than Phong shading but can miss certain highlights.

### 3. **Phong Shading**
- **Process:** Normal vectors are interpolated across the surface, and illumination is calculated per pixel (fragment).
- **Effect:** Highly realistic shading with smooth highlights, but it’s computationally expensive.

>[!summary] **Intuition for Phong Shading**  
> Phong shading focuses on pixel-by-pixel lighting to achieve a smooth, detailed finish. It captures subtle variations in lighting, giving realistic highlights and shadows at a high computational cost.

---

## Material Properties

### Phong Material Parameters
- **Ambient Coefficient ( $k_a$ ):** Controls the base ambient reflection.
- **Diffuse Coefficient ( $k_d$ ):** Controls how much light spreads across the surface.
- **Specular Coefficient ( $k_s$ ):** Determines the shininess or reflectivity.
- **Shininess ( $\alpha$ ):** Defines how tight or wide the specular highlight appears.

**Example (Emerald Material):**

>[!info]
> - $k_a = \{0.02, 0.17, 0.02, 1.0\}$  
> - $k_d = \{0.08, 0.61, 0.08, 1.0\}$  
> - $k_s = \{0.63, 0.73, 0.63, 1.0\}$  
> - $\alpha = 40$

>[!summary] **You can think of the shininess parameter as...**  
> adjusting how "sharp" the highlights are. Small values (like 1) create large, soft highlights (plastic or matte surfaces), while high values (100 or more) give small, sharp highlights (like polished metal).

---

## Attenuation

Light intensity naturally decreases with distance. Phong includes an attenuation factor using constants $a$, $b$, and $c$ to model this.

>[!info]
> $$ \text{Attenuation Factor} = \frac{1}{a + b \cdot d + c \cdot d^2} $$  
> Where $d$ is the distance from the light source.

>[!summary] **Understanding Attenuation**  
> Think of attenuation as the fading of light over distance. Imagine standing far from a light source—the further you go, the dimmer the light appears.

---

## Light Types

### 1. **Positional Light**
- **Definition:** Emits light in all directions from a single point, like a light bulb.
- **Special Case:** Spotlight, where light is emitted in a cone rather than all directions.

>[!summary] **You can think of positional light as...**  
> a "point light" that spreads evenly outward. Spotlights are a version of this with a focused direction.

### 2. **Directional Light**
- **Definition:** Light rays are parallel, as if coming from a distant source like the sun.

### **Spotlight**
- Uses a focus direction $S$ and an angle $\delta$ to create a cone of light.

