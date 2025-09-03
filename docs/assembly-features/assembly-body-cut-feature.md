# Assembly Body Cut Feature

<p align="left">
  <img src="/demo-images/cut1.png" width="270">
  <img src="/demo-images/cut2.png" width="175">
  <img src="/demo-images/cut3.png" width="250">
</p>

## Feature Overview

The assembly body cut feature cuts one part out of another in an assembly. Like the other assembly features, this must be used by editing a part in the context of an assembly

---

## Property Manager Page

The Property Manager Page for the assembly body cut feature is shown below:

<div class="image-annot"
     style="--callout-stroke: 2px;           /* outline thickness */
            --callout-size: 22px;            /* icon box size */
            --callout-font-size: 10px;       /* number size */
            --callout-stroke-color: red;     /* default circle color */
            --callout-text-color: red;       /* default number color */
            --callout-stroke-hover: blue;    /* hover circle color */
            --callout-text-hover: blue;">    <!-- hover number color -->
  <img src="/images/assembly-body-cut-pmp.png" alt="Actuator Cross Section">

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
This is the body of the part you are currently editing in context. This tells the feature what part you would like the cutting body to cut into

### <a id="height"></a>2) Cutting Body
This is the body that is used to cut out the main body

---

## Tips and General Thoughts

1. This feature is extremely useful for working with complex geometries that need to interface with each other. It lets you design the complicated features on one part and then simply cut them out into another part

2. I wanted to be able to add some kind of tolerance or offset parameter, but it became too complicated to work with and determine how that offset should be handled. I recommend using this to make the first cutout and then doing the tolerancing yourself using a surface offset or something similar

3. To make this feature permanent and not updating as the assembly updates, you should set external refences to "lock" instead of "break." Breaking the reference makes the feature not work anymore

