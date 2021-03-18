- A vertex shader's job is to generate clip space coordinates. it always takes the form:
	```
	gl_Position;
	void main(){
			gl_Position = doMathToMakeClipspaceCoordinates;
	}
	```
- The shader is called once per vertex. Each time it's called you are required to set the **special global variable**, gl_Position to some clip space coordinates.
- Vertex shaders need data. They can get that data in 3 ways.
	1. [[Attributes]]
	2. [[Uniforms]]
	3. [[Textures]]
- Based on the positions the function outputs WebGL can then rasterize various kinds of primitives including [[point, line, and triangles]]