---
name: jax-computation
description: >
  High-performance numerical computing and accelerator compilation engine.
---

# JAX Numerical Computing Tool

## Overview
JAX is Autograd and XLA, brought together for high-performance machine learning research. It can automatically differentiate native Python and NumPy code, and compile loops/functions to GPU/TPU accelerators using XLA.

## Programmatic Code Example
```python
import jax.numpy as jnp
from jax import grad, jit, vmap

# Define a simple function
def predict(params, inputs):
    return jnp.dot(inputs, params)

# Compute gradient automatically
grad_predict = grad(predict)

# Compile using XLA JIT
fast_predict = jit(predict)
```
