# Bump Bend Feature

<p align="left">
<img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/bump1.png" width="225">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/bump2.png" width="225">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/bump3.png" width="225">
</p>

## Feature Overview

The bump bend feature creates many small sheet metal bends that act like one big bend of a large radius. These can be useful when you need a larger radius in a sheet metal part but you do not have a tool that can make that large of a radius. The number of bump bends can be adjusted with more bends meaning a closer approximation of the single large bend

---

## Property Manager Page

The Property Manager Page for the bump bend feature is shown below:

<div class="image-annot"
     style="--image-max-width: 300px;
            --overlay-width: 500px;
            --callout-size: 22px;
            --callout-stroke: 2px;
            --callout-font-size: 6px;
            --callout-stroke-color: red;
            --callout-text-color: red;
            --callout-stroke-hover: blue;
            --callout-text-hover: blue;">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/images/bump-bend-pmp.png" alt="Cylinder Property Manager Page">

  <!-- Scalable overlay aligned to the image -->
  <svg viewBox="0 0 120 110" preserveAspectRatio="xMidYMid meet" aria-hidden="true">

    <!-- 1) Bend Starting Face Reference -->
    <a href="#param-1" aria-label="Bend Starting Face Reference">
      <svg class="callout-svg" x="12" y="-5">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">1</text>
      </svg>
    </a>

    <!-- 2) Bend Edge Reference -->
    <a href="#param-2" aria-label="Bend Edge Reference">
      <svg class="callout-svg" x="12" y="9">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">2</text>
      </svg>
    </a>

    <!-- 3) Large Bend Radius -->
    <a href="#param-3" aria-label="Large Bend Radius">
      <svg class="callout-svg" x="12" y="24">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">3</text>
      </svg>
    </a>

    <!-- 4) Bend Angle -->
    <a href="#param-4" aria-label="Bend Angle">
      <svg class="callout-svg" x="12" y="38">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">4</text>
      </svg>
    </a>

    <!-- 5) Bump Bend Radius -->
    <a href="#param-5" aria-label="Bump Bend Radius">
      <svg class="callout-svg" x="12" y="53">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">5</text>
      </svg>
    </a>

    <!-- 6) Number of Bends -->
    <a href="#param-6" aria-label="Number of Bends">
      <svg class="callout-svg" x="12" y="67">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">6</text>
      </svg>
    </a>

    <!-- 7) Material Thickness -->
    <a href="#param-7" aria-label="Material Thickness">
      <svg class="callout-svg" x="12" y="79">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">7</text>
      </svg>
    </a>

    <!-- 8) End Flange Length -->
    <a href="#param-8" aria-label="End Flange Length">
      <svg class="callout-svg" x="12" y="90">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">8</text>
      </svg>
    </a>

    <!-- 9) Type of Bend -->
    <a href="#param-9" aria-label="Type of Bend">
      <svg class="callout-svg" x="12" y="107">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">9</text>
      </svg>
    </a>

  </svg>
</div>

---

## Parameters

### <a id="param-1"></a>1) Bend Starting Face Reference

This is the face that the bump bend will "grow" from. It will likely be the smaller face on the side of a sheet metal part.

### <a id="param-2"></a>2) Bend Edge Reference

This is the edge that the bend should bend around. It should be one of the edges of the bend starting face

### <a id="param-3"></a>3) Large Bend Radius

This is the overall bend radius you are trying to acheive. It is the theoretical bend that the bump bend will approximate as the number of bends increases

### <a id="param-4"></a>4) Bend Angle

This is the angle the bump bend will curve around the bend edge

### <a id="param-5"></a>5) Bump Bend Radius

This is the small radius of the individual bump bends. This should be the radius of the bending tool being used. The default is 3 mm.

### <a id="param-6"></a>6) Number of Bends

The number of small bump bends that will be used to approximate the large bend

### <a id="param-7"></a>7) Material Thickness

This is an optional parameter that lets you adjust the thickness of the bump bend. By default it will be the thickness of the sheet metal

### <a id="param-8"></a>8) End Flange Length

This is the length of the last straightaway after the bump bend is complete

### <a id="param-9"></a>9) Type of Bend

There are two types of bump bends, internal and external. "Internal to Perfect Bend" approximates the ideal bend radius from the inside of that curve, and "External to Perfect Bend" approximates the ideal bend from the outside. As the number of bends increases these two options will both converge to the ideal bend

---

## Tips and General Thoughts

1. If you want to be able to fold and unfold these bump bends like any other sheet metal part, you will need to export this file to a step file and then import it again as a solidworks part. After that you can convert it to sheet metal and it will act like any other sheet metal part. The downside is that you loose the ability to make parametric adjustments to the bump bend

2. It is possible to design bump bends with this tool that are not manufacturable. Make sure that whoever you are using to make the sheet metal parts is able to manufacture your part before getting too invested in it