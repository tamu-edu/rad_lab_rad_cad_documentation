# RAD Logo Feature

<p align="left">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/rad-logo1.png" width="250">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/rad-logo2.png" width="200">
  <img src="./demo-images/rad-logo3.png" width="200">
</p>

## Feature Overview

The RAD Logo feature can be used to add this logo onto a part, or cut it into a part. All the values are parametric making it easy to customize it to how you want it to look

---

## Property Manager Page

The Property Manager Page for the RAD Logo feature is shown below:

<div class="image-annot"
     style="--image-max-width: 225px;
            --overlay-width: 500px;
            --callout-size: 22px;
            --callout-stroke: 2px;
            --callout-font-size: 6px;
            --callout-stroke-color: red;
            --callout-text-color: red;
            --callout-stroke-hover: blue;
            --callout-text-hover: blue;">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/images/RAD-logo-pmp.png" alt="Cylinder Property Manager Page">

  <!-- Scalable overlay aligned to the image -->
  <svg viewBox="0 0 120 110" preserveAspectRatio="xMidYMid meet" aria-hidden="true">

    <!-- 1) Bend Starting Face Reference -->
    <a href="#param-1" aria-label="Bend Starting Face Reference">
      <svg class="callout-svg" x="12" y="3">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">1</text>
      </svg>
    </a>

    <!-- 2) Bend Edge Reference -->
    <a href="#param-2" aria-label="Bend Edge Reference">
      <svg class="callout-svg" x="12" y="17">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">2</text>
      </svg>
    </a>

    <!-- 3) Large Bend Radius -->
    <a href="#param-3" aria-label="Large Bend Radius">
      <svg class="callout-svg" x="12" y="33">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">3</text>
      </svg>
    </a>

    <!-- 4) Bend Angle -->
    <a href="#param-4" aria-label="Bend Angle">
      <svg class="callout-svg" x="12" y="49">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">4</text>
      </svg>
    </a>

    <!-- 5) Bump Bend Radius -->
    <a href="#param-5" aria-label="Bump Bend Radius">
      <svg class="callout-svg" x="12" y="65">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">5</text>
      </svg>
    </a>

    <!-- 6) Number of Bends -->
    <a href="#param-6" aria-label="Number of Bends">
      <svg class="callout-svg" x="12" y="81">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">6</text>
      </svg>
    </a>

    <!-- 7) Material Thickness -->
    <a href="#param-7" aria-label="Material Thickness">
      <svg class="callout-svg" x="12" y="102">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">7</text>
      </svg>
    </a>

  </svg>
</div>

---

## Parameters

### <a id="param-1"></a>1) Sketch Point

This sketch point will be at the center of the RAD logo.

### <a id="param-2"></a>2) Base Depth

The depth of the base extrusion of the logo

### <a id="param-3"></a>3) Logo Depth

The depth of the words part of the logo

### <a id="param-4"></a>4) Orbit Depth

The depth of the orbit part of the logo

### <a id="param-5"></a>5) Total Length

The maximum length along the width of the text

### <a id="param-6"></a>6) Angle

The angle of the logo around the sketch point

### <a id="param-7"></a>7) Body Operation

There are two options, add body or subtract body. Add body is meant to add a positive space logo onto a surface. Subtract body is meant to cut a logo into something else

---

## Tips and General Thoughts

1. You cannot make any of the depths 0, but if you make them very close to zero and it will basically act the same