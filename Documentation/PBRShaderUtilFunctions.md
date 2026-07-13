# psPBRTemplate.glsl Utility Functions

This document provides an overview of the utility functions defined in the `psPBRTemplate.glsl` shader file. These functions are designed to facilitate various operations related to PBR rendering, camera properties, and pointer ring effects.

---

### `getPBRProperties`

```glsl
PBRProperties getPBRProperties()
```

- **Description**: Retrieves the PBR material properties for the current fragment. The material properties are fetched from the `MaterialBuffer` using the `materialId`.
- **Return Type**: `PBRProperties`

---

### `getTimeMs`

```glsl
uint64_t getTimeMs()
```

- **Description**: Returns the current time in milliseconds as provided by the frame parameters.
- **Return Type**: `uint64_t`

---

### `getViewProjection`

```glsl
mat4 getViewProjection()
```

- **Description**: Retrieves the view-projection matrix for the current frame. This matrix transforms world-space coordinates to clip-space.
- **Return Type**: `mat4`

---

### `getInvViewProjection`

```glsl
mat4 getInvViewProjection()
```

- **Description**: Retrieves the inverse of the view-projection matrix, which transforms clip-space coordinates back to world-space.
- **Return Type**: `mat4`

---

### `getView`

```glsl
mat4 getView()
```

- **Description**: Retrieves the view matrix for the current frame. This matrix transforms world-space coordinates to view-space.
- **Return Type**: `mat4`

---

### `getInvView`

```glsl
mat4 getInvView()
```

- **Description**: Retrieves the inverse of the view matrix, which transforms view-space coordinates back to world-space.
- **Return Type**: `mat4`

---

### `getCameraPosition`

```glsl
vec3 getCameraPosition()
```

- **Description**: Returns the world-space position of the camera for the current frame.
- **Return Type**: `vec3`

---

### `getScreenSize`

```glsl
vec2 getScreenSize()
```

- **Description**: Retrieves the dimensions of the screen in pixels as a 2D vector.
- **Return Type**: `vec2`

---

### `isPointerRingEnabled`

```glsl
bool isPointerRingEnabled()
```

- **Description**: Checks if the pointer ring effect is enabled for the current frame.
- **Return Type**: `bool`

---

### `getPointerRayDirection`

```glsl
vec3 getPointerRayDirection()
```

- **Description**: Retrieves the direction of the pointer ray in world-space coordinates.
- **Return Type**: `vec3`

---

### `getPointerRayOrigin`

```glsl
vec3 getPointerRayOrigin()
```

- **Description**: Retrieves the origin of the pointer ray in world-space coordinates.
- **Return Type**: `vec3`

---

### `getPointerRingOuterDistThreshold`

```glsl
float getPointerRingOuterDistThreshold()
```

- **Description**: Returns the outer distance threshold for the pointer ring effect. Fragments beyond this distance are not affected by the pointer ring.
- **Return Type**: `float`

---

### `getPointerRingInnerDistThreshold`

```glsl
float getPointerRingInnerDistThreshold()
```

- **Description**: Returns the inner distance threshold for the pointer ring effect. Fragments within this distance are not affected by the pointer ring.
- **Return Type**: `float`

---

### `getPointerRingColorMix`

```glsl
float getPointerRingColorMix()
```

- **Description**: Retrieves the mix factor for blending the pointer ring color with the fragment's original color.
- **Return Type**: `float`

---

### `getPointerRingColor`

```glsl
vec3 getPointerRingColor()
```

- **Description**: Returns the color of the pointer ring.
- **Return Type**: `vec3`

---

### `getFragToPointerRayDistance`

```glsl
float getFragToPointerRayDistance()
```

- **Description**: Calculates the shortest distance between the current fragment's world position and the pointer ray.
- **Return Type**: `float`

---

### `isInPointerRing`

```glsl
bool isInPointerRing()
```

- **Description**: Determines whether the current fragment is within the pointer ring, based on its distance from the pointer ray and the inner/outer distance thresholds.
- **Return Type**: `bool`

---

### `mixWithPointerRing`

```glsl
vec4 mixWithPointerRing(in vec4 color)
```

- **Description**: Modifies the input color by blending it with the pointer ring color if the pointer ring effect is enabled and the fragment is within the ring. The blending is influenced by the surface normal and view direction for natural shading.
- **Return Type**: `vec4`
