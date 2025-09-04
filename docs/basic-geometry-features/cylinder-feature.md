# Cylinder Feature

<p align="left">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/cylinder1.png" width="250">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/cylinder2.png" width="200">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/cylinder3.png" width="250">
</p>

## Feature Overview

The cylinder feature creates a cylinder centered at the origin.

This is not created as a joining body, it will be created as its own body even if it overlaps another body on creation

---

## Property Manager Page

The Property Manager Page for the cylinder feature is shown below:

<div class="image-annot"
     style="--image-max-width: 300px;
            --overlay-width: 500px;
            --callout-size: 22px;
            --callout-stroke: 2px;
            --callout-font-size: 13px;
            --callout-stroke-color: red;
            --callout-text-color: red;
            --callout-stroke-hover: blue;
            --callout-text-hover: blue;">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/images/cylinder-pmp.png" alt="Cylinder Property Manager Page">

  <!-- Scalable overlay aligned to the image -->
  <svg viewBox="0 0 120 100" preserveAspectRatio="xMidYMid meet" aria-hidden="true">

    <!-- 1) Diameter -->
    <a href="#diameter" aria-label="Width">
      <svg class="callout-svg" x="-30" y="40">
        <!-- transparent hit target for reliable hover/click -->
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="8"></circle>
        <text x="11" y="12">1</text>
      </svg>
    </a>

    <!-- 2) Height -->
    <a href="#height" aria-label="Height">
      <svg class="callout-svg" x="-30" y="73">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="8.5"></circle>
        <text x="11" y="12">2</text>
      </svg>
    </a>

  </svg>
</div>

---

## Parameters

### <a id="diameter"></a>1) Diameter
The outer diameter of the cylinder

### <a id="height"></a>2) Height
The height of the cylinder

---

## Tips and General Thoughts

1. This feature is good for creating a starting cylinder centered about the origin.


