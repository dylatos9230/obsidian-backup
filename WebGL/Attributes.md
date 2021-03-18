## Introduction
- The most common way is through buffers and attributes

## Usage
1. Create buffers.
	```js
	var buf = gl.createBuffer();
	```
2. Put data in those buffers.
	```js
	gl.bindBuffer(gl.ARRAY_BUFFER, buf);
	```
	
3. Then, given a shader program you made you look up the location of its attributes at initialization time 
	```js
	var positionLoc = gl.getAttribuLocation(someShaderProgram, "a_position");
	```
4. and at render time tell WebGL how to pull data out of those buffers and into the attribute.
```js
	// turn on getting data out of a buffer for this attribute
	gl.enableVertexAttribArray(positionLoc);

	var numComponents = 3; // (x, y, z)
	var type = gl.FLOAT; // 32bit floating point values
	var normalize = false; // leave the values as they are
	var offset = 0; // start at the beginning of the buffer
	var stride = 0; // how many bytes to move to the next vertex
	// 0 = use the correct stride for type and numComponents

	gl.vertexAttribPointer(positionLoc, numComponents, type, false, stride, offset);
```
5. In WebGL fundamentals we showed that we can do no math in the shader and just pass the data directly through.
```c
attribute vec4 a_position;
void main(){
	gl_Position = a_position;
}
```
6. If we put clip space vertices into our buffers it will work.
7. **Attributes** can use **float** , **vec2**, **vec3**, **vec4**, **mat2**, **mat3**, and **mat4** as types.