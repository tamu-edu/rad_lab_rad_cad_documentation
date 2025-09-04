# Heat Insert Feature

<p align="left">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/heat1.png" width="250">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/../demo-images/heat2.png" width="175">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/../demo-images/heat3.png" width="250">
</p>

## Feature Overview

The Heat Insert Feature inserts heat inserts at specific sketch points. It can handle sketch points from different sketches and on different faces, as long as the points are on a body

It uses the McMaster-Carr [Tapered Heat-Set Inserts for Plastic](https://www.mcmaster.com/products/inserts/threaded-insert-type~heat-set/tapered-heat-set-inserts-for-plastic-7/) heat inserts. However, if you also have the option to insert custom heat insert parameters if you are not using these heat inserts

It also for some reason crashes way more than any other RAD CAD feature, so it is recommended to save every time before trying to use it

---

## Property Manager Page

The Property Manager Page for the heat inserts feature is shown below:

<div class="image-annot"
     style="
            --image-max-width: 235px;
            --overlay-width: 500px;
            --callout-stroke: 2px;           /* outline thickness */
            --callout-size: 22px;            /* icon box size */
            --callout-font-size: 8px;       /* number size */
            --callout-stroke-color: red;     /* default circle color */
            --callout-text-color: red;       /* default number color */
            --callout-stroke-hover: blue;    /* hover circle color */
            --callout-text-hover: blue;">    <!-- hover number color -->
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/../images/heat-insert-pmp.png" alt="Heat insert cross section">

  <!-- Outer overlay: scalable and centered -->
  <svg viewBox="0 0 120 100" preserveAspectRatio="xMidYMid meet" aria-hidden="true">

    <!-- Callout 1 -->
    <a href="#width" aria-label="Width">
      <!-- Position in outer viewBox coords; icon size fixed by CSS -->
      <svg class="callout-svg" x="-6" y="27">
        <!-- Center the glyph inside the 22×22 box -->
        <circle cx="11" cy="11" r="5"></circle>
        <text x="11" y="12">1</text>
      </svg>
    </a>

    <!-- Callout 2 -->
    <a href="#height" aria-label="Height">
      <svg class="callout-svg" x="-6" y="58">
        <circle cx="11" cy="11" r="5"></circle>
        <text x="11" y="12">2</text>
      </svg>
    </a>

    <!-- Callout 3 -->
    <a href="#depth" aria-label="Depth">
      <svg class="callout-svg" x="-6" y="78">
        <circle cx="11" cy="11" r="5"></circle>
        <text x="11" y="12">3</text>
      </svg>
    </a>

  </svg>
</div>

---

## Parameters

### <a id="width"></a>1) Sketch Points

The sketch points to add heat inserts to. The heat insert will be centered around the sketch point. The sketch point should be on a sketch created on the flat surface that the heat insert should be added to

### <a id="height"></a>2) Heat Insert Type (Metric)
This lets you select the heat insert you want to use from the metric options. If you want specific sizes for "short," "long," or "medium" you should consult the mcmaster-carr list

There is also an option in this menu to insert your own heat insert parameters for custom sizes

### <a id="depth"></a>3) Heat Insert Type (Imperial)
This lets you select the heat insert you want to use from the imperial options. If you want specific sizes for "short," "long," or "medium" you should consult the mcmaster-carr list

There is also an option in this menu to insert your own heat insert parameters for custom sizes

---

## Tips and General Thoughts

1. As mentioned above, this feature tends to crash more than any other feature. Be sure to save SolidWorks before running it. I do not know why this happens

