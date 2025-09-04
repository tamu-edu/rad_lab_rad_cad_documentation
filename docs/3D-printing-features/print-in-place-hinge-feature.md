# Print-In-Place Hinge Feature

<p align="left">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/hinge1.png" width="150">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/hinge2.png" width="175">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/hinge3.png" width="300">
</p>


## Feature Overview

The Print-In-Place Hinge feature creates a hinge that can be printed as one part in a 3D printer, but still rotate. The tolerance of that hinge can be adjusted for different tightnesses of hinges depending on the use case

---

## Property Manager Page

The Property Manager Page for the print-in-place hinge feature is shown below:

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
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/images/hinge-pmp.png" alt="Cylinder Property Manager Page">

  <!-- Scalable overlay aligned to the image -->
  <svg viewBox="0 0 120 110" preserveAspectRatio="xMidYMid meet" aria-hidden="true">

    <!-- 1) Bend Starting Face Reference -->
    <a href="#param-1" aria-label="Bend Starting Face Reference">
      <svg class="callout-svg" x="12" y="5">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">1</text>
      </svg>
    </a>

    <!-- 2) Bend Edge Reference -->
    <a href="#param-2" aria-label="Bend Edge Reference">
      <svg class="callout-svg" x="12" y="21">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">2</text>
      </svg>
    </a>

    <!-- 3) Large Bend Radius -->
    <a href="#param-3" aria-label="Large Bend Radius">
      <svg class="callout-svg" x="12" y="37">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">3</text>
      </svg>
    </a>

    <!-- 4) Bend Angle -->
    <a href="#param-4" aria-label="Bend Angle">
      <svg class="callout-svg" x="12" y="52">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">4</text>
      </svg>
    </a>

    <!-- 5) Bump Bend Radius -->
    <a href="#param-5" aria-label="Bump Bend Radius">
      <svg class="callout-svg" x="12" y="68">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">5</text>
      </svg>
    </a>

    <!-- 6) Number of Bends -->
    <a href="#param-6" aria-label="Number of Bends">
      <svg class="callout-svg" x="12" y="84">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">6</text>
      </svg>
    </a>

    <!-- 7) Material Thickness -->
    <a href="#param-7" aria-label="Material Thickness">
      <svg class="callout-svg" x="12" y="95">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">7</text>
      </svg>
    </a>

    <!-- 8) End Flange Length -->
    <a href="#param-8" aria-label="End Flange Length">
      <svg class="callout-svg" x="12" y="104">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">8</text>
      </svg>
    </a>

  </svg>
</div>

---

## Parameters

### <a id="param-1"></a>1) Face to Add Hinge To

This is the face the hinge will be added to. It should be a flat face

### <a id="param-2"></a>2) Reference Edge

This is the edge that the hinge references for creation. By default it will be right on this edge of the face

### <a id="param-3"></a>3) Tolerance

This is the overall tolerance of the hinge. It is the distance between all of the internal hinge features. 0.01 in works well for most applications, but if you want to try different options out you should print one of these [Tolerance Tests](https://www.printables.com/model/815843-print-in-place-tolerance-test) out. Looser tolerances may work better for larger hinges and tighter tolerances can be better in certain applications

### <a id="param-4"></a>4) Number of Knuckle Pairs

The number of pairs of hinge knuckles, not including the center. For longer hinges you should increase this number. You could also just put two 1 knuckle hinges on either side (as two different hinge features)

### <a id="param-5"></a>5) Knuckle Length

The length of each knuckle along the edge direction

### <a id="param-6"></a>6) Knuckle Width

The width of the knuckle along perpendicular to the edge. This sort of acts as the "hinge size" in many ways

### <a id="param-7"></a>7) Hinge Horizontal Offset

The offset of the hinge along the edge direction. Useful if you dont want the hinge to be in the direct center of the edge

### <a id="param-8"></a>8) Hinge Depth Offset

The offset of the hinge towards the center of the face. This lets you move the hinge off the edge of the face and put it in a different location

---

## Tips and General Thoughts

1. I would highly recommend printing a [Tolerance Test](https://www.printables.com/model/815843-print-in-place-tolerance-test) to see what tolerance will work best on your printer

2. As you are designing with these hinges, you can put an axis on the hinge and use direct editing to rotate the hinge in the part. This lets you see how it will look as the hinge rotates or even design the hinged component in one rotation and then print it in another rotation