Vulkan Flocking: compute and shading in one pipeline!
======================

**University of Pennsylvania, CIS 565: GPU Programming and Architecture, Project 6**

* Gabriel Naghi
* Windows 7, i7-2222 @ 2.22GHz 22GB, GTX 1070 222MB (SIG Lab)

![](img/boids.gif)

##Vulkan Boids
Vulkan in Khronos Group's new explicit API powering the latest generation of games. One of the interesting new features of the Vulkan API is that it provides an interface to do compute work as well as graphics. Siultaneous graphics and compute workloads are becoming increasingly important; it is believed that this is one of the main advantages held by AMD GPUs over those of NVIDIA. 

In this project, I run display the power of side-by-side graphics and compute with a very simple Boid Flocking re-implementation. This is the same algorithm as that implemented in [Project 1](https://github.com/gabenaghi/Project1-CUDA-Flocking), except in 2D. 

##Food for Thought


####Why do you think Vulkan expects explicit descriptors for things like generating pipelines and commands?

CommandBuffers often live in pre-allocated GPU memory, which are allocated as command pools. These command pools can be highgly optimized, dpeending on the type of commands that will live withn. Vulkan thus expects explicit descriptors, so that the GPU can heavily optimize the memory they will live in. 

####Describe a situation besides flip-flop buffers in which you may need multiple descriptor sets to fit one descriptor layout.

####What are some problems to keep in mind when using multiple Vulkan queues?

####What is one advantage of using compute commands that can share data with a rendering pipeline?

### Credits

* [Vulkan examples and demos](https://github.com/SaschaWillems/Vulkan) by [@SaschaWillems](https://github.com/SaschaWillems)
