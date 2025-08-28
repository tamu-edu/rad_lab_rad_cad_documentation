# Sphere Feature

## Feature Overview

The sphere feature creates a sphere centered on the origin. There are options to make it hollow or a partial sphere

---

## Property Manager Page

The Property Manager Page for the box feature is shown below:

<div class="image-annot"
     style="--callout-stroke: 2px;
            --callout-size: 22px;
            --callout-font-size: 8px;
            --callout-stroke-color: red;
            --callout-text-color: red;
            --callout-stroke-hover: blue;
            --callout-text-hover: blue;">
  <img src="/images/sphere-pmp.png" alt="Sphere Property Manager Page">

  <svg viewBox="0 0 120 100" preserveAspectRatio="xMidYMid meet" aria-hidden="true">

    <!-- 1) Inner Radius -->
    <a href="#inner-radius" aria-label="Inner Radius">
      <svg class="callout-svg" x="0" y="20">
        <!-- transparent rect ensures the box is hoverable/clickable -->
        <rect width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="5"></circle>
        <text x="11" y="12">1</text>
      </svg>
    </a>

    <!-- 2) Outer Radius -->
    <a href="#outer-radius" aria-label="Outer Radius">
      <svg class="callout-svg" x="0" y="40">
        <rect width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="5"></circle>
        <text x="11" y="12">2</text>
      </svg>
    </a>

    <!-- 3) Polar Angle -->
    <a href="#polar-angle" aria-label="Polar Angle">
      <svg class="callout-svg" x="0" y="60">
        <rect width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="5"></circle>
        <text x="11" y="12">3</text>
      </svg>
    </a>

    <!-- 4) Azimuth Angle -->
    <a href="#azimuth-angle" aria-label="Azimuth Angle">
      <svg class="callout-svg" x="0" y="80">
        <rect width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="5"></circle>
        <text x="11" y="12">4</text>
      </svg>
    </a>

  </svg>
</div>


---

## Parameters

### <a id="inner-radius"></a>1) Inner Radius
The inner radius controls the thickness of the sphere if set to greater than 0. If the inner radius is 0 it will create a solid sphere. The inner radius should be smaller than the outer radius

### <a id="outer-radius"></a>2) Outer Radius
The outer radius of the sphere

### <a id="polar-angle"></a>3) Polar Angle
The polar angle is the angle of the sphere about the z axis in spherical coordinates. It should be set to values between 0 and 360 degrees inclusive

### <a id="azimuth-angle"></a>4) Azimuth Angle
The polar angle is the cone-ish angle of the sphere in spherical coordinates. It should be set to values between 0 and 180 degrees inclusive

---

## Tips and General Thoughts

1) This feature is good for creating a starting sphere centered about the origin

