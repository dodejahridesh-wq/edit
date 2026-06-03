---
name: blender-api
description: >
  Blender 3D computer graphics scripting engine.
---

# Blender Python Scripting API

## Overview
Blender features a deeply integrated Python API (`bpy`) that allows developers to programmatically generate 3D geometry, control rendering setups, animate nodes, and automate assets pipeline.

## Headless Execution
```bash
# Execute Python script inside headless Blender
blender --background --python render_scene.py
```

## Python Script Example (`render_scene.py`)
```python
import bpy

# Clear existing objects
bpy.ops.object.select_all(action='SELECT')
bpy.ops.object.delete()

# Create a new cube
bpy.ops.mesh.primitive_cube_add(size=2, location=(0, 0, 0))

# Render scene
bpy.context.scene.render.image_settings.file_format = 'PNG'
bpy.context.scene.render.filepath = '/path/to/output.png'
bpy.ops.render.render(write_still=True)
```
