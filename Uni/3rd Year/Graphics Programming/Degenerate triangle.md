A degenerate triangle is a triangle that contains 2 of the same vertex, turning it into what is basically a line. These triangles are automatically discarded but are useful when changing directions when drawing generalized [triangle strips](Triangle%20Strip.md) (i.e. triangle strips that can change direction).

## Connecting multiple triangle strips 
These can also be used to connect multiple triangle strips together, as they can be used to connect the last vertex of one strip to the first vertex of the next strip.
In the example below, the first triangle strip can be drawn using: `4,0,5,6,2,7,3`. 
The second triangle strip can be drawn using: `8,4,9,5,10,6,11,7`.
To connect these 2 strips, we need to simply insert two duplicate vertices in between the two strips.
`4,0,5,6,2,7,3,`<span style="color: red">3, 8,</span>`8,4,9,5,10,6,11,7`
This results in 4 degenerate triangles in between the two strips, connecting them together. 
`[7,3,3]]`, `[3,3,8]`, `[3,8,8]`, `[8,8,4]`
This way the first strip ends in the vertex 3 and the next strip starts with the vertex 8. 

![[TriangleStripMultiple.png]]

