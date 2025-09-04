# Rivets Feature

<p align="left">
<img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/rivets1.png" width="250">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/rivets2.png" width="200">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/rivets3.png" width="200">
</p>

## Feature Overview

The rivet feature is used to insert rivets into an existing hole feature. This can be useful to confirm hole spacing will allow for rivet insertion. It is also useful to see if the rivet mandrel will fit into the assembly you have created to make sure your assembly is assemble-able

These rivets are based on the McMaster-Carr [Aluminum Domed Head Blind Rivets](https://www.mcmaster.com/products/rivets/rivets-2~/aluminum-domed-head-blind-rivets/)

---

## Property Manager Page

The Property Manager Page for the rivet feature is shown below:

<div class="image-annot"
     style="--callout-stroke: 2px;
            --callout-size: 22px;
            --callout-font-size: 8px;
            --callout-stroke-color: red;
            --callout-text-color: red;
            --callout-stroke-hover: blue;
            --callout-text-hover: blue;">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/images/rivets-pmp.png" alt="Sphere Property Manager Page">

  <svg viewBox="0 0 120 100" preserveAspectRatio="xMidYMid meet" aria-hidden="true">

    <!-- 1) Hole Pattern -->
    <a href="#param-1" aria-label="Hole Pattern">
      <svg class="callout-svg" x="0" y="20">
        <rect width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="5"></circle>
        <text x="11" y="12">1</text>
      </svg>
    </a>

    <!-- 2) Material Thickness -->
    <a href="#param-2" aria-label="Material Thickness">
      <svg class="callout-svg" x="0" y="40">
        <rect width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="5"></circle>
        <text x="11" y="12">2</text>
      </svg>
    </a>
    
    <!-- 3) Reverse Direction -->
    <a href="#param-3" aria-label="Reverse Direction">
      <svg class="callout-svg" x="0" y="51">
        <rect width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="5"></circle>
        <text x="11" y="12">3</text>
      </svg>
    </a>

    <!-- 4) Pop Rivets -->
    <a href="#param-4" aria-label="Pop Rivets">
      <svg class="callout-svg" x="0" y="62">
        <rect width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="5"></circle>
        <text x="11" y="12">4</text>
      </svg>
    </a>

    <!-- 5) Rivet Type -->
    <a href="#param-5" aria-label="Rivet Type">
      <svg class="callout-svg" x="0" y="80">
        <rect width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="5"></circle>
        <text x="11" y="12">5</text>
      </svg>
    </a>

  </svg>
</div>


---

## Parameters

### <a id="param-1"></a>1) Hole Pattern

The hole pattern you want to insert rivets into. YOU MUST select the hole pattern from the feature tree to the right of the property manager page. For some reason solidworks will not allow you to select custom features on the part itself. If you select it from the feature tree however it will work fine

For most rivet features this will be the only parameter you need to select

### <a id="param-2"></a>2)  Material Thickness

This is an optional parameter that is used if you need to flip the rivet direction. The Reverse Direction parameter (3) only flips the direction the rivets are created but does not move them from their original spots. This material thickness parameter translates the rivets correctly to the other side of the material

It should only be needed when flipping rivet direction

### <a id="param-3"></a>3) Reverse Direction

This flips the direciton of the rivets. As discussed in material thickness (2), you will need to tweak material thickness to correctly translate the rivets to the other side of the sheet

By default the rivets go in the direction normal to the plane used in the source hole pattern feature

### <a id="param-4"></a>4) Pop Rivets

A rivet is "popped" when it has been inserted and fixed to the sheets it is attaching. When this happens the mandrel is removed. All this option does is remove the mandrel from the rivets

### <a id="param-5"></a>5) Rivet Type

By default this will match the hole pattern's rivet diameter. If the hole pattern is set to "define diameter directly" and this type is set to "match hole pattern," it will just use the 3/32 rivets as the default. 

You can also select a type of rivet to use directly if you want to look at what different rivet types might look like. All of these rivet options are based on the McMaster-Carr [Aluminum Domed Head Blind Rivets](https://www.mcmaster.com/products/rivets/rivets-2~/aluminum-domed-head-blind-rivets/)



---

## Tips and General Thoughts

1. This feature approximates rivets by only using three cylinders. Real rivets of this kind have a domed head that is not modeled here.

2. The rivet feature is meant to be used to check if rivets will fit or to animate the process of putting in rivets to an assembly. They should not be in parts that are sent to be manufactured so be sure to suppress or delete them before sending files to have parts be created.

3. The rivet feature can be used within a part, but it can also be used from a different part similar to how cross drill is used. If you set up an assembly and edit a part in context, you can create rivets based on hole patterns in other parts. Aggie Toolbox will do all the math behind the scenes to make sure the rivets in the edited part line up with the hole pattern in the external part. This can be used to make rivets as a separate part and make it easier to animate assemblies to show how rivets can be used in the assembly process.

4. If you are not using aluminum domed head blind rivets, be very careful when using the preset rivet types. Not all rivets with the same diameter are the same, and this might cause you to design parts that cannot actually be riveted together. If you are unsure if your rivets are the same as the preset ones in RAD CAD, I would recommend entering your values in the custom rivets option just to be safe.

5. Rivets are not a joining body, meaning that even if they touch your sheet they should not fuse into it as one body
