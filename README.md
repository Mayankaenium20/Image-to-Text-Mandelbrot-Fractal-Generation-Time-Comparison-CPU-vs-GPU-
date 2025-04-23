# Image-to-Text: Mandelbrot Fractal Generation Time Comparison (CPU vs GPU)

## Project Overview

This project explores the performance of Mandelbrot set generation across three different approaches: sequential CPU processing, Numba-accelerated computation, and parallel GPU (CUDA) execution. It benchmarks and visualizes execution times to demonstrate the significant performance advantages of GPU acceleration in compute-intensive mathematical tasks.

## Abstract

This project investigates the efficiency of Mandelbrot set generation using CPU and GPU architectures. Through implementation and comparison of the Mandelbrot algorithm on both platforms, it evaluates execution times and visual outcomes. The study quantifies the performance disparity between CPU and GPU processing for complex mathematical computations like the Mandelbrot set. The results highlight the computational advantages of GPU parallelism in scientific computing.

## Introduction

The **Mandelbrot set** is a famous example of a fractal in mathematics — a complex, infinitely detailed structure generated through iterative functions over complex numbers. It is visually captivating and mathematically rich, often used to explore chaos theory, complex dynamics, and nonlinear systems.

Fractals like the Mandelbrot set are not just artistic patterns; they have significant applications in scientific research:

- **Modeling Natural Phenomena**: Fractals are used to simulate complex natural forms such as coastlines, mountains, clouds, plants, and blood vessels. The recursive and self-similar nature of fractals makes them ideal for generating realistic graphics in computer simulations.
- **Signal and Image Compression**: Fractal algorithms are leveraged in image compression techniques due to their ability to represent complex patterns with minimal data.
- **Physics and Chaos Theory**: Mandelbrot sets are studied in dynamical systems and chaos theory to understand stability, sensitivity, and transitions between order and chaos in systems.
- **Medical Imaging and Biology**: Fractal analysis is used in quantifying irregular patterns in biological structures like heartbeats, neural networks, or lung branching, contributing to diagnostic tools.

This project compares the computational efficiency of generating the Mandelbrot set on **CPU (sequential)**, **Numba-optimized**, and **GPU (CUDA-parallelized)** environments. By doing so, it not only highlights hardware-specific performance advantages but also underlines the value of accelerating computations for scientific research where fractals are often applied in simulations, modeling, and analysis.

## Problem Definition

The primary objective is to analyze and compare Mandelbrot set generation times across different hardware architectures. The goal is to evaluate how GPU acceleration improves performance relative to traditional CPU processing. This comparison provides clarity on the trade-offs between computation time, memory usage, and scalability for large-scale fractal generation tasks.

## Algorithm Overview

Three approaches are used for performance comparison:

1. **Normal Sequential Approach**  
   - A basic iterative method using nested loops on the CPU.
   - Each pixel is processed one after another.

2. **Numba Approach**  
   - Just-In-Time (JIT) compilation using Numba to optimize the sequential code.
   - Offers performance boosts through runtime compilation.

3. **CUDA Approach**  
   - Utilizes CUDA to execute computations on the GPU.
   - Each pixel is processed in parallel by GPU threads for significant speed-up.

## Performance Metrics

| Approach            | Compute Time (seconds) |
|---------------------|------------------------|
| Sequential          | 6.59                   |
| Numba               | 0.33                   |
| CUDA                | 0.24                   |

- The CUDA-based implementation performs fastest due to parallel GPU execution.
- Numba offers a substantial improvement over sequential code by optimizing Python functions.
- Sequential implementation is slowest due to its linear processing.

## Results and Visualization

The results clearly show that:
- GPU acceleration provides the best performance for large-scale fractal generation.
- Numba offers a useful middle ground for optimization without hardware-specific dependencies.
- Visualizations of the generated fractals confirm that all approaches produce consistent outputs with varying execution speeds.

## Conclusion

This project showcases how GPU parallelism significantly reduces computation time in iterative tasks such as Mandelbrot set generation. The comparative study helps identify optimal strategies for performance in scientific and graphical computations.

## License

This project is licensed under the [MIT License](LICENSE).
