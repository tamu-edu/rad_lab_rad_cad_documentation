# 8020 Feature

<p align="left">
  <img src="/demo-images/80201.png" width="225">
  <img src="/demo-images/80202.png" width="175">
  <img src="/demo-images/80203.png" width="260">
</p>

## Feature Overview

The 8020 feature creates 8020 extrusion centered at the origin. 8020 extrusion is aluminum extrusion often used for prototyping. The edge faces of this 8020 feature are all parallel to each other. There are two types of 8020 in this feature: 10 series and 15 series.

This is not created as a joining body, it will be created as its own body even if it overlaps another body on creation

---

## Property Manager Page

The Property Manager Page for the 8020 feature is shown below:

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
  <img src="/images/8020-pmp.png" alt="Cylinder Property Manager Page">

  <!-- Scalable overlay aligned to the image -->
  <svg viewBox="0 0 120 100" preserveAspectRatio="xMidYMid meet" aria-hidden="true">

    <!-- 1) Diameter -->
    <a href="#diameter" aria-label="Width">
      <svg class="callout-svg" x="-25" y="36">
        <!-- transparent hit target for reliable hover/click -->
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="8"></circle>
        <text x="11" y="12">1</text>
      </svg>
    </a>

    <!-- 2) Height -->
    <a href="#height" aria-label="Height">
      <svg class="callout-svg" x="-25" y="75">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="8.5"></circle>
        <text x="11" y="12">2</text>
      </svg>
    </a>

  </svg>
</div>

---

## Parameters

### <a id="diameter"></a>1) Length
The overall length of the 8020

### <a id="height"></a>2) Type of 8020
The type of 8020. Our lab typically only uses 10 or 15 series so that is all that is avaliable here

---

## Tips and General Thoughts

1. If you need 2x1 or 2x2 geometries, you could either use this feature and then mirror the bodies, or use the mcmaster downloads.

2. this feature is mainly useful for its easily adjustable length.


