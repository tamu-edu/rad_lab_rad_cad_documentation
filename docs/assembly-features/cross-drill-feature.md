# Cross Drill Feature

<p align="left">
  <img src="/demo-images/cross1.png" width="225">
  <img src="/demo-images/cross2.png" width="250">
  <img src="/demo-images/cross3.png" width="200">
</p>

## Feature Overview

The cross drill feature is used in tandem with the hole pattern feature. If you have two parts lined up in an assembly, it will use the hole pattern's geometry to cut those holes into another part. To use this feature, you need to be in an assembly and edit in context the part that you want to cut into.

---

## Property Manager Page

The Property Manager Page for the cross drill feature is shown below:

<div class="image-annot"
     style="--callout-stroke: 2px;
            --callout-size: 22px;
            --callout-font-size: 9px;
            --callout-stroke-color: red;
            --callout-text-color: red;
            --callout-stroke-hover: blue;
            --callout-text-hover: blue;">
  <img src="/images/cross-drill-pmp.png" alt="Sphere Property Manager Page">

  <svg viewBox="0 0 120 100" preserveAspectRatio="xMidYMid meet" aria-hidden="true">

    <!-- 1) Inner Radius -->
    <a href="#ref1" aria-label="Inner Radius">
      <svg class="callout-svg" x="-5" y="22">
        <!-- transparent rect ensures the box is hoverable/clickable -->
        <rect width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="6"></circle>
        <text x="11" y="12">1</text>
      </svg>
    </a>

    <!-- 1) Inner Radius -->
    <a href="#ref2" aria-label="Inner Radius">
      <svg class="callout-svg" x="-5" y="38">
        <!-- transparent rect ensures the box is hoverable/clickable -->
        <rect width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="6"></circle>
        <text x="11" y="12">2</text>
      </svg>
    </a>

    <!-- 1) Inner Radius -->
    <a href="#ref3" aria-label="Inner Radius">
      <svg class="callout-svg" x="-5" y="55">
        <!-- transparent rect ensures the box is hoverable/clickable -->
        <rect width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="6"></circle>
        <text x="11" y="12">3</text>
      </svg>
    </a>

    <!-- 1) Inner Radius -->
    <a href="#ref4" aria-label="Inner Radius">
      <svg class="callout-svg" x="-5" y="78">
        <!-- transparent rect ensures the box is hoverable/clickable -->
        <rect width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="6"></circle>
        <text x="11" y="12">4</text>
      </svg>
    </a>


  </svg>
</div>


---

## Parameters

### <a id="ref1"></a>1) Cross Drill Variables - Cut Depth

Cut Depth controls how far from the hole pattern this feature cuts

### <a id="ref2"></a>2) Cross Drill Variables - Reverse Direction

Reverse Direction is an optional parameter that can flip the direction of the cross drilling

### <a id="ref3"></a>3) Hole Pattern

This is the hole pattern that cross drill is using to cut the current part. It has to be selected through the feature tree in the part that it is located in. 

### <a id="ref4"></a>4) Body to Cut

The body in the currently edited part that cross drill should cut through. This allows for managing multiple bodies in one part and lets you specify what you would like to be cutting with this feature

---

## Tips and General Thoughts

1. If you would like to update the cross drill feature after moving things around, enter the part in edit mode again and click edit on the feature. Once you click the check mark it will update the location of the cross drill

2. If you want to guarantee that the cross drilled holes never move, you should break the reference in the part

