## Introduction
- For a shader uniforms are values passed to the shader that stay the same for all vertices in a  draw call.

## Usage
1. As a very simple example we could add an offset to the vertex shader above
```c
	attribute vec4 a_position;
	uniform vec4 u_offset;

	void main(){
		gl_Position = a_position + uoffset;
	}
```
2. And now we could offset every vertex by a certain amount. First we'd look up the location of the uniform at initialization time
```js
	var offsetLoc = gl.getUniformLocation(someProgram, "u_offset");
```

3. And then before drawing we'd set the uniform
```js
	gl.uniform4fv(offsetLoc, [1,0,0,0]); // offset it to the right half the screen 
```
4. Note that uniforms belong to individual shader programs. If you have **multiple shader programs** with uniforms of the same both uniforms will have their own locations and hold their own values.
5. Uniforms can be many types. For each type you have to call the corresponding function to set it.
![[Pasted image 20210302160100.png]]
6. There's also types **bool**, **bvec2**,**bvec3**, and **bvec4**. They use either the **gl.uniform?f?** or **gl.uniform?i?** functions.
7. Note that for an array you can set all the uniforms of the array at once. 
```js
	// in shader
	uniform vec2 u_someVec2[3];

	// in js at init time
	var someVec2Loc = gl.getUniformLocation(someProgram, "u_someVec2");

	// at render time
	gl.uniform2fv(someVec2Loc, [1,2,3,4,5,6]) // set the entire array of u_someVec2	
```

8. But if you want to set individual elements of the array you must look up the location of each element individually.

```js
// in js at init time
	var someVec2Element0Loc = gl.getUniformLocation(someProgram, "u_someVec2[0]");
	var someVec2Element1Loc = gl.getUniformLocation(someProgram, "u_someVec2[1]");
	var someVec2Element2Loc = gl.getUniformLocation(someProgram, "u_someVec2[2]");
// at render time
	gl.uniform2fv(someVec2Element0Loc, [1,2]); // set element 0
	gl.uniform2fv(someVec2Element1Loc, [3,4]); // set element 1
	gl.uniform2fv(someVec2Element2Loc, [5,6]); // set element 2
```
9. Similarly if you create a struct
```c++
	struct SomeStruct {
		bool active;
		vec2 someVec2;
	}

```
you have to look up each field individually
```js
	var someThingActiveLoc = gl.getUniformLocation(someProgram, "u_someThing.active");
	var someThingSomeVec2Loc = gl.getUniformLocation(someProgram, "u_someThing.someVec2");
```