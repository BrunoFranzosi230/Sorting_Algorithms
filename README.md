# 🌌 Master Sorting Visualizer

> A high-performance, interactive sorting algorithm visualizer featuring a Deep Space / Cyberpunk aesthetic, real-time code execution tracking, and synthesized audio feedback.

## 📖 Overview

Master Sorting Visualizer is a single-page web application designed to help users understand how various sorting algorithms operate. Unlike standard visualizers, this project integrates **audio synthesis** (using the Web Audio API) to create a unique soundscape based on the data being sorted, alongside a **live code overlay** that highlights the exact line of code being executed in real-time.

## ✨ Key Features

* **Deep Space / Cyberpunk Theme:** A polished UI with Slate-900 backgrounds, neon accents, and glowing element effects.
* **Audio Synthesis:** Generates sound using a Pentatonic Minor scale with a custom Echo/Delay effect. Higher values produce higher pitches.
* **Live Code Tracing:** A dedicated panel displays the algorithm's pseudo-code and highlights the active line as the animation plays.
* **Async Animation Engine:** Uses JavaScript `async/await` for smooth, non-blocking animations that can be paused or stopped instantly.
* **No Dependencies:** Built entirely with Vanilla JavaScript, HTML5 Canvas, and CSS3. No frameworks or libraries required.

## 🧮 Supported Algorithms

The visualizer includes a wide range of algorithms categorized by complexity:

### Simple Sorts
* **Bubble Sort:** The classic stepping stone algorithm.
* **Insertion Sort:** Builds the sorted array one item at a time.
* **Selection Sort:** Repeatedly finds the minimum element.
* **Cocktail Shaker Sort:** A bidirectional Bubble Sort.

### Efficient Sorts
* **Merge Sort:** A divide and conquer algorithm (recursive).
* **Quick Sort:** Efficient sorting using a pivot and partitioning.
* **Heap Sort:** utilizes a binary heap data structure.

### Non-Comparison Sorts
* **Radix Sort (LSD):** Sorts integers by processing individual digits (uses buckets).

## 🚀 How to Run

Since this project is a standalone web file, installation is instant.

1.  Download the `index.html` file.
2.  Open the file in any modern web browser (Chrome, Firefox, Edge, Safari).
3.  **Note:** To hear the audio, you must interact with the page (click "Start" or "Shuffle") at least once, as browsers block auto-playing audio contexts.

## 🎮 Controls

* **Algorithm Select:** Choose from the dropdown menu to load specific algorithm logic.
* **Shuffle Array:** Generates a new random set of data bars.
* **Start:** Begins the visualization.
* **Stop:** Immediately halts the current execution and unlocks controls.

## 🛠️ Technical Implementation

### The Canvas
The visualization uses the HTML5 `<canvas>` element for high-performance rendering. Bars are drawn dynamically, and specific indices (compare/swap targets) are repainted with distinct colors (Pink for comparison, Blue for pivots/sorted ranges, Green for completion).

### The Audio Engine
This project utilizes the `window.AudioContext` API.
* **Oscillator:** Generates Sine waves.
* **Gain Node:** Controls volume envelopes (ADSR-like fade out).
* **Delay Node:** Creates a spatial echo effect.
* **Frequency Mapping:** Data values are mapped to specific frequencies in a hardcoded musical scale.

### Code Highlighting
The algorithms are stored as arrays of strings. As the sorting function runs, it calls a helper function `highlight(lineNumber)` which toggles CSS classes on the DOM elements in the code panel.

## 📄 License

This project is open source and free to use for educational purposes.

---
*Created with JavaScript.*
