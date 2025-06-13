---
layout: page
title: Global Solution to SLAM
description: Development of globally optimal solutions to simultaneous localization and mapping for robot navigation in complex environments.
img: assets/img/global_slam/Overview.png
importance: 3
category: research
---

<div class="post-content">
  <h2>Project Overview</h2>
  <p>
    <strong>Supported by ARC Discovery Project</strong>
  </p>

  <p>
    This research theme focuses on complex robotic systems design and integration, robot navigating and interacting with objects in highly complex environments, biologically inspired robots, underwater robots, drones, and soft grippers. The project aims to develop globally optimal solutions that ensure robust and accurate simultaneous localization and mapping (SLAM) for various robotic applications.
  </p>

  <h2>Research Focus</h2>
  <h3>Robotic Systems</h3>
  <p>
    This research theme focuses on complex robotic systems design and integration, robot navigating and interacting with objects in highly complex environments, including:
  </p>
  <ul>
    <li><strong>Biologically Inspired Robots:</strong> Development of bio-inspired locomotion and navigation systems</li>
    <li><strong>Underwater Robots:</strong> Robust SLAM solutions for challenging underwater environments</li>
    <li><strong>Drones:</strong> Aerial navigation and mapping in complex 3D environments</li>
    <li><strong>Soft Grippers:</strong> Integration of manipulation capabilities with navigation systems</li>
  </ul>

  <h2>Technical Approach</h2>
  <h3>Algorithm Development</h3>
  <ul>
    <li>
      <strong>Gauss-Newton Optimization:</strong> Implementation of advanced Gauss-Newton methods for nonlinear optimization in SLAM problems
    </li>
    <li>
      <strong>Variable Projection Techniques:</strong> Development of variable projection algorithms for improved convergence and computational efficiency
    </li>
    <li>
      <strong>Feature-based SLAM:</strong> Advanced feature detection and matching algorithms for robust localization and mapping
    </li>
    <li>
      <strong>Global Optimization:</strong> Ensuring convergence to globally optimal solutions rather than local minima
    </li>
  </ul>

  <h2>Key Innovations</h2>
  <ul>
    <li>
      <strong>Globally Optimal Solutions:</strong> Development of algorithms that guarantee convergence to global optima in SLAM problems
    </li>
    <li>
      <strong>Computational Efficiency:</strong> Advanced optimization techniques that reduce computational complexity while maintaining accuracy
    </li>
    <li>
      <strong>Robustness:</strong> Algorithms that perform reliably in challenging environments with noise and uncertainty
    </li>
    <li>
      <strong>Multi-platform Applications:</strong> Solutions adaptable to various robotic platforms from underwater vehicles to aerial drones
    </li>
  </ul>

  <h2>Applications</h2>
  <p>
    The research outcomes have broad applications across multiple domains:
  </p>
  <ul>
    <li><strong>Search and Rescue Operations:</strong> Reliable navigation in disaster scenarios</li>
    <li><strong>Underwater Exploration:</strong> Mapping and navigation in marine environments</li>
    <li><strong>Autonomous Vehicles:</strong> Robust localization for self-driving cars</li>
    <li><strong>Industrial Automation:</strong> Precise navigation and manipulation in manufacturing</li>
  </ul>
  <h2>Visualization</h2>
  <div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
      {%
        include figure.liquid
        loading="eager"
        path="assets/img/global_slam/Demo.jpg"
        alt="Global Solution to SLAM"
        title="Global Solution to SLAM"
        class="img-fluid rounded z-depth-1"
        max-height="400px"
        sizes="(max-width: 767px) 100vw, 50vw"
      %}
    </div>
  </div>
  <div class="caption">
    Global Solution to SLAM - Visualization of globally optimal solutions for simultaneous localization and mapping, showing algorithm convergence and feature-based SLAM implementations
  </div>

</div> 