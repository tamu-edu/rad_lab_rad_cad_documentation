# Box Feature

<p align="left">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/box3.png" width="250">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/box1.png" width="200">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/box2.png" width="250">
</p>

## Feature Overview

The box feature creates a box using width height and depth parameters. It also centers that box on the origin. This can be a very useful starting point for a part

This is not created as a joining body, it will be created as its own body even if it overlaps another body on creation

---

## Property Manager Page

The Property Manager Page for the box feature is shown below:

<div class="image-annot"
     style="--callout-stroke: 2px;           /* outline thickness */
            --callout-size: 22px;            /* icon box size */
            --callout-font-size: 10px;       /* number size */
            --callout-stroke-color: red;     /* default circle color */
            --callout-text-color: red;       /* default number color */
            --callout-stroke-hover: blue;    /* hover circle color */
            --callout-text-hover: blue;">    <!-- hover number color -->
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/images/box-pmp.png" alt="Actuator Cross Section">

  <!-- Outer overlay: scalable and centered -->
  <svg viewBox="0 0 120 100" preserveAspectRatio="xMidYMid meet" aria-hidden="true">

    <!-- Callout 1 -->
    <a href="#width" aria-label="Width">
      <!-- Position in outer viewBox coords; icon size fixed by CSS -->
      <svg class="callout-svg" x="-10" y="27">
        <!-- Center the glyph inside the 22×22 box -->
        <circle cx="11" cy="11" r="6"></circle>
        <text x="11" y="12">1</text>
      </svg>
    </a>

    <!-- Callout 2 -->
    <a href="#height" aria-label="Height">
      <svg class="callout-svg" x="-10" y="52">
        <circle cx="11" cy="11" r="6"></circle>
        <text x="11" y="12">2</text>
      </svg>
    </a>

    <!-- Callout 3 -->
    <a href="#depth" aria-label="Depth">
      <svg class="callout-svg" x="-10" y="77">
        <circle cx="11" cy="11" r="6"></circle>
        <text x="11" y="12">3</text>
      </svg>
    </a>

  </svg>
</div>

---

## Parameters

### <a id="width"></a>1) Width
The width parameter controls the size of the box in the x direction

### <a id="height"></a>2) Height
The height parameter controls the size of the box in the z direction

### <a id="depth"></a>3) Depth
The depth parameter controls the size of the box in the y direction

---

## Tips and General Thoughts

1. This feature is good for creating a starting box centered about the origin.

