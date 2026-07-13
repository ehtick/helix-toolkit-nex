# psPointTemplate.glsl Utility Functions

## `getUV`

```glsl
vec2 getUV()
```

- **Description**: Retrieves the UV coordinates of the current fragment.
- **Return Type**: `vec2`

---

## `getColor`

```glsl
vec4 getColor()
```

- **Description**: Retrieves the interpolated vertex color for the current fragment.
- **Return Type**: `vec4`

---

## `getPointSize`

```glsl
float getPointSize()
```

- **Description**: Retrieves the screen-space size of the point being rendered.
- **Return Type**: `float`

---

## `getTextureId`

```glsl
uint getTextureId()
```

- **Description**: Retrieves the texture ID associated with the current fragment.
- **Return Type**: `uint`

---

## `getSamplerId`

```glsl
uint getSamplerId()
```

- **Description**: Retrieves the sampler ID associated with the current fragment.
- **Return Type**: `uint`

---

## `getTimeMs`

```glsl
uint64_t getTimeMs()
```

- **Description**: Retrieves the current time in milliseconds from the frame parameters.
- **Return Type**: `uint64_t`

---

## `getViewProjection`

```glsl
mat4 getViewProjection()
```

- **Description**: Retrieves the view-projection matrix from the frame parameters.
- **Return Type**: `mat4`

---

## `getInvViewProjection`

```glsl
mat4 getInvViewProjection()
```

- **Description**: Retrieves the inverse of the view-projection matrix from the frame parameters.
- **Return Type**: `mat4`

---

## `getView`

```glsl
mat4 getView()
```

- **Description**: Retrieves the view matrix from the frame parameters.
- **Return Type**: `mat4`

---

## `getInvView`

```glsl
mat4 getInvView()
```

- **Description**: Retrieves the inverse of the view matrix from the frame parameters.
- **Return Type**: `mat4`

---

## `getCameraPosition`

```glsl
vec3 getCameraPosition()
```

- **Description**: Retrieves the world-space position of the camera from the frame parameters.
- **Return Type**: `vec3`

---

## `getScreenSize`

```glsl
vec2 getScreenSize()
```

- **Description**: Retrieves the dimensions of the screen in pixels from the frame parameters.
- **Return Type**: `vec2`

---

## `isPointerRingEnabled`

```glsl
bool isPointerRingEnabled()
```

- **Description**: Checks if the pointer ring effect is enabled in the frame parameters.
- **Return Type**: `bool`

---

## `getPointerRayDirection`

```glsl
vec3 getPointerRayDirection()
```

- **Description**: Retrieves the direction of the pointer ray in world space from the frame parameters.
- **Return Type**: `vec3`

---

## `getPointerRayOrigin`

```glsl
vec3 getPointerRayOrigin()
```

- **Description**: Retrieves the origin of the pointer ray in world space from the frame parameters.
- **Return Type**: `vec3`

---

## `getPointerRingOuterDistThreshold`

```glsl
float getPointerRingOuterDistThreshold()
```

- **Description**: Retrieves the outer distance threshold for the pointer ring effect.
- **Return Type**: `float`

---

## `getPointerRingInnerDistThreshold`

```glsl
float getPointerRingInnerDistThreshold()
```

- **Description**: Retrieves the inner distance threshold for the pointer ring effect.
- **Return Type**: `float`

---

## `getPointerRingColorMix`

```glsl
float getPointerRingColorMix()
```

- **Description**: Retrieves the color mix factor for blending the pointer ring color with the fragment color.
- **Return Type**: `float`

---

## `getPointerRingColor`

```glsl
vec3 getPointerRingColor()
```

- **Description**: Retrieves the color of the pointer ring effect.
- **Return Type**: `vec3`

---

## `getFragToPointerRayDistance`

```glsl
float getFragToPointerRayDistance()
```

- **Description**: Calculates the shortest distance between the current fragment's world position and the pointer ray.
- **Return Type**: `float`

---

## `isInPointerRing`

```glsl
bool isInPointerRing()
```

- **Description**: Determines if the current fragment lies within the pointer ring's inner and outer distance thresholds.
- **Return Type**: `bool`

---

## `mixWithPointerRing`

```glsl
vec4 mixWithPointerRing(in vec4 color)
```

- **Description**: Blends the input color with the pointer ring color if the pointer ring effect is enabled and the fragment is within the pointer ring.
- **Return Type**: `vec4`
