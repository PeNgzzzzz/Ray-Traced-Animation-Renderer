# Ray Traced Animation Renderer

A C++ ray tracer implementing several classic rendering techniques including texture mapping, bump mapping, recursive reflections, shadows, and motion blur.

The renderer generates an animated celestial scene with reflective objects and orbiting planets.

## Demo

![Ray Tracing Demo](demo.gif)

## Rendering Features

- Recursive ray tracing for reflections
- Texture mapping using UV coordinates and bilinear interpolation
- Bump mapping for surface detail
- Shadow ray casting for realistic lighting
- Motion blur via time-sampled ray tracing
- Scene graph structure supporting hierarchical objects

## Rendering Pipeline

1. Construct scene graph with geometry nodes and materials  
2. Cast primary rays from camera through each pixel  
3. Compute intersections with scene geometry  
4. Evaluate lighting using Phong shading model  
5. Spawn reflection rays recursively  
6. Cast shadow rays for light occlusion  
7. Sample multiple time steps for motion blur

## Project Structure
```

.
├── Animate/
├── Assets/
├── GeometryNode.cpp / .hpp
├── SceneNode.cpp / .hpp
├── Primitive.cpp / .hpp
├── Mesh.cpp / .hpp
├── Light.cpp / .hpp
├── Material.cpp / .hpp
├── PhongMaterial.cpp / .hpp
├── Image.cpp / .hpp
├── Main.cpp Entry point
├── Makefile
├── README.md
└── ...

```

## Rendering Output

- Resolution: 500 × 500
- Frame rate: 24 FPS
- Duration: ~30 seconds
- Frames rendered using custom ray tracer
- Final animation assembled using OpenShot (see sound.mp4)

## Resources

Planet textures: SolarSystemScope  
Tennis ball texture: Robin Wood textures  
Checker pattern: Vecteezy  
Wood texture: Pexels
