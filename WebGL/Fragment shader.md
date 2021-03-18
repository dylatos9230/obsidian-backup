## Introduction
- When rasterizing these primitives it calls a second user supplied function called a fragment shader.
- A fragment shader's job is to compute a color for each pixel of the primitive currently being drawn.
- It always takes the form.
```c
	precision mediump float;

   	void main() {
   		gl\_FragColor \= doMathToMakeAColor;
   	}
```
Your fragment shader is called once per pixel. Each time it's called you are required to set the special global variable, `gl_FragColor` to some color.
- Fragment shaders need data. They can get data in 3 ways.
	- [[Uniforms]]
	- [[Textures]]
	- [[Varyings]]
	