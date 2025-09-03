# Base Sheet Feature

<p align="left">
<img src="/demo-images/base-sheet3.png" width="175">
  <img src="/demo-images/base-sheet1.png" width="225">
  <img src="/demo-images/base-sheet2.png" width="175">
</p>

## Feature Overview

The base sheet feature creates a sheet metal base centered at the origin. It does this by creating a box and then converting it to sheet metal. After it is created it acts the exact same way any other sheet metal part would.

---

## Property Manager Page

The Property Manager Page for the base sheet feature is shown below:

<div class="image-annot"
     style="--image-max-width: 300px;
            --overlay-width: 500px;
            --callout-size: 22px;
            --callout-stroke: 2px;
            --callout-font-size: 9px;
            --callout-stroke-color: red;
            --callout-text-color: red;
            --callout-stroke-hover: blue;
            --callout-text-hover: blue;">
  <img src="/images/base-sheet-pmp.png" alt="Cylinder Property Manager Page">

  <!-- Scalable overlay aligned to the image -->
  <svg viewBox="0 0 120 100" preserveAspectRatio="xMidYMid meet" aria-hidden="true">

    <!-- 1) Diameter -->
    <a href="#diameter" aria-label="Width">
      <svg class="callout-svg" x="-10" y="26">
        <!-- transparent hit target for reliable hover/click -->
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="6"></circle>
        <text x="11" y="12">1</text>
      </svg>
    </a>

    <!-- 1) Diameter -->
    <a href="#height" aria-label="Width">
      <svg class="callout-svg" x="-10" y="50">
        <!-- transparent hit target for reliable hover/click -->
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="6"></circle>
        <text x="11" y="12">2</text>
      </svg>
    </a>

    <!-- 1) Diameter -->
    <a href="#mat-thick" aria-label="Width">
      <svg class="callout-svg" x="-10" y="75">
        <!-- transparent hit target for reliable hover/click -->
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="6"></circle>
        <text x="11" y="12">3</text>
      </svg>
    </a>


  </svg>
</div>

---

## Parameters

### <a id="diameter"></a>1) Width
The overall width of the base sheet in the z direction

### <a id="height"></a>2) Height
The overall height of the base sheet in the x direction

### <a id="mat-thick"></a>3) Material Thickness
The overall material thickness of the base sheet in the y direction

---

## Tips and General Thoughts

1. This feature is a hybrid between a custom feature and a macro. This is a brief description of how it works in case it is relevent for debugging any issues: After entering the desired parameter values for width, height, and material thickness, the base sheet feature will start to get created. First the feature makes a non-sheet metal solid rectangular prism with the desired dimensions. It then selects the top face of the rectangular prism and converts it to sheet metal. This is why the design tree always shows a convert solid feature below the base sheet feature. This extra convert to sheet metal process is because SolidWorks does not easily allow for the direct create of a sheet metal part and this was an easier and more stable process to implement.

2. After creation, if the feature is edited and the material thickness is changed, after the base sheet updates it will also go into the sheet metal folder in the design tree and change the material thickness stored there. This will update the material thickness for the entire entire part. This process of changing the sheet metal folder tends to cause the part to flicker as a graphical update when it the sheet metal folder updates.

3. You should never have two base sheets in the same part. Since base sheet is meant to be the starting point for a sheet metal part, it is created in the same location and orientation every time. Having two base sheets in one part means they will overlap and could cause some strange issues.

4. When you edit the material thickness of a base sheet, there will be a short graphical update where the base sheet seems to move. This is a result of this feature updating the Sheet Metal's thickness and is nothing to be worried about. The base sheet will stay centered on the origin.

5. If you delete the convert solid after the base sheet, the base sheet will act like a regular extrusion. This could cause problems or confusion later so best practice is to just delete both the base sheet and the convert solid together if you delete the convert solid.

6. This is a bit of an odd one, but if you delete the base sheet feature it is best practice to make sure you also delete the Sheet Metal folder. If you don't delete the sheet metal folder and insert a new base sheet and then try to edit the material thickness of the new base sheet, sometimes it will not update. This issue can be fixed by deleting the base sheet as well as the Sheet Metal folder and then inserting a fresh base sheet. I honestly doubt this ever causes any problems for anyone, but it's a problem I ran into when stress testing this feature so I wanted to include it here.


