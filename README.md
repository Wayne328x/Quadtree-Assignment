# 🧩 Quadtree Image Decomposition – CSC A48 Assignment 2

> **Disclaimer**  
> This project was completed as part of the CSC A48 – Intro to Computer Science II course at the University of Toronto Scarborough.  
> It is shared **after the course has concluded** and is intended **only for portfolio and learning purposes**.  
> ❗️Do **not copy, reuse, or submit** any part of this code for academic credit. Doing so may constitute academic dishonesty.

---

## 📌 Overview

This project implements a **quadtree-based image decomposition tool** using **Binary Search Trees (BSTs)** to segment grayscale images into uniform regions. It was designed to demonstrate algorithmic thinking, memory management in C, and recursive image processing techniques.

---

## 🛠️ Features

- 🧠 **Recursive BST-based Quadtree structure**  
  Each image region is stored as a `Quad` node with splitting behavior and unique spatial keys.

- 🎨 **Image Processing**  
  Reads and writes `.pgm` grayscale images, performs region averaging, and applies threshold-based similarity checks.

- ✂️ **Region Splitting Logic**  
  Dynamically splits image regions by width or height based on color variation (difference between max and min pixel values).

- 🧾 **Interactive Driver**  
  Command-line interface to load images, insert/search/delete tree nodes, perform tree traversal, split regions, and save output images.

---

## 📂 File Structure

| File | Description |
|------|-------------|
| `Quad.c` | Core implementation of BST + Quadtree logic (insert, delete, traverse, split). |
| `imgUtils.c` | Image utility functions: read `.pgm`, write `.pgm`, copy image. |
| `A2_interactive_driver.c` | Menu-driven interactive CLI to test tree operations and output results. |

---

## 🖼️ Image Input/Output

- Input format: `.pgm` grayscale images
- Output: Processed image saved as `output.pgm`
- Supported modes:
  - Outlines only
  - Outlines + averaged color
  - Averaged color fill

---

## 📥 How to Compile & Run

```bash
gcc A2_interactive_driver.c -o quadtree_tool
./quadtree_tool
