## Introduction
- A varying is way to pass a value from a vertex shader to a fragment shader which we coverd in how it works.
- To use a varying we need to declare matching varyings in both a vertex and fragment shader. We set the varying in the vertex shader with some value per vertex.
- when WebGL draws pixels it will interpolate between those values and pass them to the corresponding varying in the fragment shader.


#### Vertex Shader
```c
	attribute vec4 a_position;
	uniform vec4 u_offset;
	varying vec4 v_positionWithOffset;
	
	void main(){
		gl_Position = a_position + u_offset;
		v_positionWithOffset = a_position + u_offset;
	}
```
#### Fragment Shader
```c
	precision mediump float;
	varying vec4 v_positionWithOFfset;
	
	void main(){
		// convert from clip space (-1 <-> +1) to color space (0->1).
		vec4 color = v_positionWithOffset * 0.5 + 0.5
		gl_FragColor = color;
	}
```