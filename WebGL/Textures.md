## Introduction
- data from pixels / texels.

## Usage
- Getting a value from a texture in a shader we create a **sampler2D** uniform and use the GLSL function **texture2D** to extract a value from it.

```c
	precision mediump float;
	uniform sampler2D u_texture;
	
	void main(){
	
		vec2 texcoord = vec2(0.5, 0.5) // get a value from the middle of the texture.
		gl_FragColor = texture2D(u_texture, texcoord)

```
- What data comes out of the texture is dependent on many settings. At a minimum we need to create and put data in the texture, for example
```js
	var tex = gl.createTexture();
	gl.bindTexture(gl.TEXTURE_2D, tex);
	var level = 0;
	var width = 2;
	var height = 1;
	var data = new Unit8Array([
		255, 0, 0, 255, // a red pixel
		0, 255, 0, 255, // a green pixel
	]);
	gl.texImage2D(gl.TEXTURE_2D, level, gl.RGBA, width, height, 0, gl.RGBA, gl.UNSIGNED_BYTE, data);
	
```

- At initialization time look up the uniform location in the shader program

```js
	var someSamplerLoc = gl.getUniformLocation(someProgram, "u_texture");
```

- At render time bind the texture to a texture unit

```js
	var unit = 5 // Pick some texture unit
	gl.activeTexture(gl.TEXTURE0 + unit);
	gl.bindTexture(gl.TEXTURE_2D, tex);
```

- And tell the shader which unit you bound the texture to 
```js
	gl.uniform1i(someSamplerLoc, unit);
```