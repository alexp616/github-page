<!-- Pictures
All the core Markdown constructs in GitHub Flavored MarkdownLinks to an external site.
Task lists -->

# **Alex Pan**
<img src="assets/selfportrait.png" alt="selfportrait" width="200"/>

## Table of Contents
- [About Me](#about-me)
- [Works](#research)
- [Favorite Language](#favorite-language)
- [Quote](#random-quote)
- [Relative Link](#relative-link)
- [Task List](#task-list)

### About Me
I am a second year undergraduate student majoring in Computer Science 
at UCSD. I'm interested in Algebraic Geometry and high-performance 
computing.

### Works
I have some mobile apps from a high school class that I'm not the 
most proud of, but they can be found in my GitHub with enough digging.

Since college, the majority of my independent work comes from projects 
in computer algebra.

- [GPUPolynomials.jl](https://github.com/alexp616/GPUPolynomials.jl), a 
"proof-of-concept" unpublished Julia library for gpu-parallelized polynomial arithmetic algorithms.
- [CudaNTTs.jl](https://github.com/alexp616/CudaNTTs.jl), a published 
Julia library for computing Number-Theoretic Transforms.

Additionally, as of now, I have one prospective publication:
1. [K3 surfaces of any Artin-Mazur height over $\mathbb{F}_5$ and $\mathbb{F}_7$ via Quasi-F-split singularities and GPU acceleration](https://arxiv.org/abs/2502.12428)
2. Hopefully many more to come...

### Favorite Language
I'm a big fan of [Julia](https://julialang.org/) because it 
makes it easy to write one-off scripts and experiments, 
while having lots of capabilities for writing 
reasonably high-performant code.

Particularly, a the popular [CUDA.jl](https://github.com/JuliaGPU/CUDA.jl) 
library serves as a low barrier to entry introduction for 
GPU programming with NVIDIA GPU's. To give an example, this is 
how you copy an array from "CPU memory" (RAM) to "GPU memory" 
(DRAM) in CUDA C++:

```C++
int h[5] = {5, 4, 3, 2, 1}; // host pointer
int size = 20; // 5 numbers * 4 bytes

int *d; // device pointer
cudaMalloc(&d, size);
cudaMemcpy(d, h, size, cudaMemcpyHostToDevice);

// do stuff with d

cudaFree(d); // free device memory when done
```

And this is the equivalent code in Julia using CUDA.jl:
```python
h = [5, 4, 3, 2, 1]
d = cu(h)

# do stuff with d
```

By just calling `cu`, CUDA.jl handles all of the memory 
allocation and copying, 
and Julia's garbage collector handles freeing unused objects.

Other than Julia, which I use primarily for scientific computing, 
I want to start really learning Rust and C++ for other more 
critical and general projects.

### Random Quote
Here is a quote I found quite funny from [When Einstein Walked 
with Gödel: Excursions to the Edge of Thought](https://www.amazon.com/When-Einstein-Walked-G%C3%B6del-Excursions/dp/0374146705):
> It used to be said that a mathematics department was the second 
cheapest for a university to fund, since its members required only 
pencils, papers, and wastebaskets. (The cheapest would be the 
philosophers, because they don't need the wastebaskets.)

### Relative Link
This is here to fulfill the assignment requirement:
[Link to README](/README.md)

### Task List
This is also here to fulfill the assignment requirement:
Things I want to start learning more about:

Math:
- [ ] Complex Analysis
- [ ] Topology
- [ ] Many, many more...

CS:
- [ ] openMP
- [ ] LLVM
- [ ] OS
- [ ] Networking Protocols

Intersection:
- [ ] Fast arithmetic
- [ ] Cryptography
- [ ] Prolog