# Tab Feature

<p align="left">
<img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/tab1.png" width="200">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/tab2.png" width="250">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/tab3.png" width="250">
</p>

## Feature Overview

The tab feature allows you to instantly make sheet metal tabs in a repeatable way. They break off very easily on 0.090" to 0.125" aluminum sheet metal but has not yet been tested on anything else.

Sheet metal tabs are used when a part does not have an edge parallel to the bend edge. These tabs act as a reference gauge when bending the sheet metal part. They then come off very easily after the part is bent. For the sheet metal they have been tested on so far, they were easily fatigue-bent off

---

## Property Manager Page

The Property Manager Page for the tab feature is shown below:

<div class="image-annot"
     style="--callout-stroke: 2px;
            --callout-size: 22px;
            --callout-font-size: 6.5px;
            --callout-stroke-color: red;
            --callout-text-color: red;
            --callout-stroke-hover: blue;
            --callout-text-hover: blue;">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/images/tab-pmp.png" alt="Sphere Property Manager Page">

  <svg viewBox="0 0 120 100" preserveAspectRatio="xMidYMid meet" aria-hidden="true">

    <!-- 1) Hole Pattern -->
    <a href="#param-1" aria-label="Hole Pattern">
      <svg class="callout-svg" x="12" y="8">
        <rect width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">1</text>
      </svg>
    </a>

    <!-- 1) Hole Pattern -->
    <a href="#param-2" aria-label="Hole Pattern">
      <svg class="callout-svg" x="12" y="23">
        <rect width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">2</text>
      </svg>
    </a>

    <!-- 1) Hole Pattern -->
    <a href="#param-3" aria-label="Hole Pattern">
      <svg class="callout-svg" x="12" y="37">
        <rect width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">3</text>
      </svg>
    </a>

    <!-- 1) Hole Pattern -->
    <a href="#param-4" aria-label="Hole Pattern">
      <svg class="callout-svg" x="12" y="51">
        <rect width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">4</text>
      </svg>
    </a>

    <!-- 1) Hole Pattern -->
    <a href="#param-5" aria-label="Hole Pattern">
      <svg class="callout-svg" x="12" y="66">
        <rect width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">5</text>
      </svg>
    </a>

    <!-- 1) Hole Pattern -->
    <a href="#param-6" aria-label="Hole Pattern">
      <svg class="callout-svg" x="12" y="84">
        <rect width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">6</text>
      </svg>
    </a>


  </svg>
</div>


---

## Parameters

### <a id="param-1"></a>1) Sheet Face

This is the face that the tab is parallel to. It will likely be the big top of the sheet metal.

### <a id="param-2"></a>1) Edge to Tab

This is the edge that the tab will attach to. It should be an edge that touches the face selected for sheet face (1).

This edge can be non-linear as well, see tips and general thoughts for more on this

### <a id="param-3"></a>1) Parallel Edge

This is the edge that the tab will be parallel to. It should likely be the bend edge of the sheet metal part.

### <a id="param-4"></a>1) Tab Offset X

Tab Offset X allows you adjust where the tab is along the tab edge. By default it is in the center of the tab edge. This also make it easy to add multiple tabs to one edge

### <a id="param-5"></a>1) Tab Offset Y

Tab Offset Y allows you to move the tab closer or further away from the tab edge

### <a id="param-6"></a>1) Connect Tab Type

There are three different ways to connect the tab to the main sheet metal part.

The first is "perpendicular to build edge" which makes the tab connections perpendicular to the edge of the sheet metal part

The second is "perpendicular to parallel edge" which makes the tab connections perpendicular to the reference parallel edge

The last option is "custom offsets" which lets you adjust directly where the tab connects to the sheet metal part

---

## Tips and General Thoughts

1. The edge being tabbed can be curved or straight. If it is curved, you will likely need to adjust the tab offsets or connection parameters to force it to fully overlap with the base sheet. 

For a non-linear edge this feature treats the two endpoints of the edge as a linear edge and uses that for reference

2. If you need a demonstration of what the tab feature does, create a simple sheet metal part with a bend in it with an edge flange. Then cut angles into the outer edge of that flange to make the end of the flange non-linear or not parallel to the bend edge. Upload it to a software like [oshcut's instant sheet metal analyzer](https://app.oshcut.com/cart). It will give you an error that says the part is not manufacturable. Then add a tab to one of those non-parallel edges and set it to be parallel to the bend edge and upload it again. Now it will show that the part is manufactuable.