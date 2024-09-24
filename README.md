# Curvetopia (Adobe GenSolve 2024 Round 2)

![Adobe GenSolve](https://github.com/user-attachments/assets/0fc954a7-d2f7-4dd0-8aee-e49003399b04)

Welcome to **Curvetopia**! This project is dedicated to identifying, regularizing, and beautifying 2D curves. Our mission is to process curves from line art, regularize them, identify symmetry, and complete incomplete curves, ultimately representing them as a set of cubic Bézier curves.


## 📌 **Project Overview**

### Objective

The primary goal of Curvetopia is to convert a set of input polylines into regularized and beautified curves. This involves handling various types of shapes, from simple lines to complex star shapes, and representing them as connected cubic Bézier curves in the final output.

### Problem Description

Instead of working with PNG raster images, Curvetopia starts by processing polylines, which are sequences of 2D points. The input consists of finite subsets of paths in \( \mathbb{R}^2 \), and the expected output is a set of regularized, symmetric, and complete paths.


## 🔍 **Sections**

### **1. Regularize Curves**

In this section, we focus on identifying and regularizing different shapes from the given set of curves. The shapes include:

1. **Straight Lines**: Identifying and fitting straight lines.
2. **Circles and Ellipses**: Detecting circles (all points equidistant from a center) and ellipses (two focal points).
3. **Rectangles and Rounded Rectangles**: Identifying rectangles, including those with curved edges.
4. **Regular Polygons**: Detecting polygons with equal sides and angles.
5. **Star Shapes**: Recognizing star shapes with a central point and multiple radial arms.

**Activity**: Test algorithms on hand-drawn shapes and doodles to verify their performance and distinguish between regularizable and non-regularizable shapes.

### **2. Exploring Symmetry in Curves**

This section focuses on identifying reflection symmetries in closed shapes. Key tasks include:

- **Reflection Symmetries**: Identifying lines of symmetry where the shape can be divided into mirrored halves.
- **Symmetry Fitting**: Transforming points and fitting identical Bézier curves on symmetric points.

**Symmetry Hunt**: Recognize that an identical-looking curve can be represented by different Bézier curve sequences.

### **3. Completing Incomplete Curves**

In this section, the objective is to complete 2D curves that have gaps due to occlusions. The challenge is to naturally complete these curves using:

- **Fully Contained Shapes**: e.g., one circle completely inside another.
- **Partially Contained Shapes**: e.g., a half-circle occluded by another shape.
- **Disconnected Shapes**: e.g., a circle split by a rectangle.

**Guide**: The completion algorithm will consider the smoothness, regularity, and symmetry of the shapes.

## 📸 **Visual Representation**

The images below demonstrate the process of solving the first two parts of Curvetopia, including regularizing curves and exploring symmetry:

### **Input Curves**
<p align="center">
  <img src="https://github.com/rishn/Adobe-GenSolve-Curvetopia/blob/main/outputs/isolated.jpg?raw=true" alt="Input Curves" />
</p>

### **Regularized Curves**
<p align="center">
  <img src="https://github.com/rishn/Adobe-GenSolve-Curvetopia/blob/main/outputs/isolated_sol.jpg?raw=true" alt="Regularized Curves" />
</p>

### **Identified Shapes**
<p align="center">
  <img src="https://github.com/rishn/Adobe-GenSolve-Curvetopia/blob/main/outputs/isolated_sol1.jpg?raw=true" alt="Identified Shapes" />
</p>

### **Symmetry Detection**
<p align="center">
  <img src="https://github.com/rishn/Adobe-GenSolve-Curvetopia/blob/main/outputs/isolated_sol2.jpg?raw=true" alt="Symmetry Detection" />
</p>

## 🚀 **Getting Started**

- The `Identify_Shapes_And_Symmetries` notebook provides solutions for regularizing curves and exploring symmetries.
- The `Occlusion` notebooks offer solutions for curve completion and handling occlusions.

Run the notebooks to explore and observe the results.

---
