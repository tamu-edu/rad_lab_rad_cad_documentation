# Assembly Body Add Feature

<p align="left">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/add3.png" width="225">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/add2.png" width="225">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/add1.png" width="260">
</p>

## Feature Overview

The assembly body add feature cuts one part out of another in an assembly. Like the other assembly features, this must be used by editing a part in the context of an assembly

---

## Property Manager Page

The Property Manager Page for the assembly body add feature is shown below:

<div class="image-annot"
     style="--callout-stroke: 2px;           /* outline thickness */
            --callout-size: 22px;            /* icon box size */
            --callout-font-size: 10px;       /* number size */
            --callout-stroke-color: red;     /* default circle color */
            --callout-text-color: red;       /* default number color */
            --callout-stroke-hover: blue;    /* hover circle color */
            --callout-text-hover: blue;">    <!-- hover number color -->
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/images/assembly-body-add-pmp.png" alt="Actuator Cross Section">

  <!-- Outer overlay: scalable and centered -->
  <svg viewBox="0 0 120 100" preserveAspectRatio="xMidYMid meet" aria-hidden="true">

    <!-- Callout 1 -->
    <a href="#width" aria-label="Width">
      <!-- Position in outer viewBox coords; icon size fixed by CSS -->
      <svg class="callout-svg" x="-15" y="40">
        <!-- Center the glyph inside the 22×22 box -->
        <circle cx="11" cy="11" r="6"></circle>
        <text x="11" y="12">1</text>
      </svg>
    </a>

    <!-- Callout 2 -->
    <a href="#height" aria-label="Height">
      <svg class="callout-svg" x="-15" y="72">
        <circle cx="11" cy="11" r="6"></circle>
        <text x="11" y="12">2</text>
      </svg>
    </a>

  </svg>
</div>

---

## Parameters

### <a id="width"></a>1) Main Body
This is the body of the part you are currently editing in context. This tells the feature what part you would like the adding body to add to

### <a id="height"></a>2) Cutting Body
This is the body that is used to add onto the main body

---

## Tips and General Thoughts

1. This feature is useful if you are working with parts in an assembly and decide they should be one part instead of two. You can just add one part to another and continue working with it as one part

2. To make this feature permanent and not updating as the assembly updates, you should set external refences to "lock" instead of "break." Breaking the reference makes the feature not work anymore

