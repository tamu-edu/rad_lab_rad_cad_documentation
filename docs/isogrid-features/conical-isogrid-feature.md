# Conical Isogrid Feature

<p align="left">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/iso-cone1.png" width="250">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/iso-cone2.png" width="175">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/iso-cone3.png" width="250">
</p>

## Feature Overview

The conical isogrid feature automatically cuts isogrid into a conical surface. There are many ways this can be customized, with different sized isogrid patterns. It creates a circular pattern around the diameter of the cone, and then moves along the height of the cone and creates new circular patterns. Because the diameter of the cone changes, the size of the triangles changes to make the pattern continuous

This feature typically only works well if the cutting triangles are small enough to have around 8 triangular cuts around the diameter of the cone. Otherwise the triangular cuts will distort too much around the curved surface and mess up the pattern. More information on this in Tips and General Thoughts

This feature also sometimes struggles with cones that end in a point. If you are having trouble getting it to work, try cutting off the top and adding a flat top face. If it is important to have the cone end in a tip, you can always add it back after the isogrid

---

## Property Manager Page

The Property Manager Page for the conical isogrid feature is shown below:

<div class="image-annot"
     style="--image-max-width: 235px;
            --overlay-width: 500px;
            --callout-size: 22px;
            --callout-stroke: 2px;
            --callout-font-size: 6px;
            --callout-stroke-color: red;
            --callout-text-color: red;
            --callout-stroke-hover: blue;
            --callout-text-hover: blue;">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/images/conical-isogrid-pmp.png" alt="Flat Isogrid Property Manager Page">

  <!-- Scalable overlay aligned to the image -->
  <svg viewBox="0 0 120 100" preserveAspectRatio="xMidYMid meet" aria-hidden="true">

    <!-- 1) preview-options -->
    <a href="#preview-options" aria-label="Preview Options">
      <svg class="callout-svg" x="10" y="-55">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">1</text>
      </svg>
    </a>

    <!-- 2) face-references -->
    <a href="#face-references" aria-label="Face References">
      <svg class="callout-svg" x="10" y="-38">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">2</text>
      </svg>
    </a>

    <!-- 4) pattern-edge-reference -->
    <a href="#pattern-edge-reference" aria-label="Pattern Edge Reference">
      <svg class="callout-svg" x="10" y="-4">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">3</text>
      </svg>
    </a>

    <!-- 5) pattern-starting-point-reference -->
    <a href="#pattern-starting-point-reference" aria-label="Pattern Starting Point Reference">
      <svg class="callout-svg" x="10" y="12">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">4</text>
      </svg>
    </a>

    <!-- 6) point-direction-offset-reference -->
    <a href="#point-direction-offset-reference" aria-label="Point Direction Offset Reference">
      <svg class="callout-svg" x="10" y="29">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">5</text>
      </svg>
    </a>

    <!-- 7) point-angle-offset-reference -->
    <a href="#point-angle-offset-reference" aria-label="Point Angle Offset Reference">
      <svg class="callout-svg" x="10" y="46">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">6</text>
      </svg>
    </a>

    <!-- 8) allow-partial-bodies -->
    <a href="#allow-partial-bodies" aria-label="Allow Partial Bodies">
      <svg class="callout-svg" x="10" y="63">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">7</text>
      </svg>
    </a>

    <!-- 9) material-thickness -->
    <a href="#material-thickness" aria-label="Material Thickness">
      <svg class="callout-svg" x="10" y="80">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">8</text>
      </svg>
    </a>

    <!-- 10) hole-to-hole-distance -->
    <a href="#hole-to-hole-distance" aria-label="Hole to Hole Distance">
      <svg class="callout-svg" x="10" y="97">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="11.75">9</text>
      </svg>
    </a>

    <!-- 11) parameter-definition-type -->
    <a href="#parameter-definition-type" aria-label="Parameter Definition Type">
      <svg class="callout-svg" x="10" y="115">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="11.75">10</text>
      </svg>
    </a>

    <!-- 11) parameter-definition-type -->
    <a href="#inside-face" aria-label="Parameter Definition Type">
      <svg class="callout-svg" x="10" y="131">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="11.75">11</text>
      </svg>
    </a>

    <!-- 11) parameter-definition-type -->
    <a href="#edge-mesh-refinement-options" aria-label="Parameter Definition Type">
      <svg class="callout-svg" x="10" y="150">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="11.75">12</text>
      </svg>
    </a>

  </svg>
</div>

---

## Parameters

### <a id="preview-options"></a>1) Isogrid Face References

The conical face that the isogrid should go on. The feature sometimes has trouble with cones that end in a point, so if you are having trouble getting it to work, try adding a top face instead of ending in a point and see if that fixes it

Once this face is selected, the part body is hidden so you can see the isogrid pattern more clearly

### <a id="face-references"></a>2) Preview Options

There are four preview options avaliable for this feature. 

No preview means that no preview will be shown before the feature is created

Preview First Column Only will show a column up the height of the cone. This can be a good way to get an idea of what all the different sized triangular cuts will look like as the diameter changes

Preview First Row Only shows a row around the circumference of the cone. If used with Preview First Column Only it will act as a seed preview that loads very quickly

Preview Triangles is a cool option. It shows a wire frame that approximates the shape the triangles will have. It acts as a good rough template of the full feature so you can get an idea of what it might look like. It loads way faster than the full feature would so it is easier to adjust before you want to load the full thing

### <a id="pattern-edge-reference"></a>4) Estimated Spar Width

Minimum spar width provides a rough distance for all of the spars between cuts. This number is more of an approximation than an exact number. This is because all the cuts are created as lofts to a point at the center axis of the cone, and this causes the distances between the cuts to change as they get closer to the center of the sphere. Curved distortion also plays a small role


### <a id="pattern-starting-point-reference"></a>5) Hole to Hole Distance

This is the rough hole to hole distance for each hole cut to its six adjacent hole cuts. 

This parameter controls the hole to hole distance of the row of cuts at the large end of the cone. This value will shrink as the isogrid travels to the small end of the cone and the cuts become closer together

This value is rounded to ensure the isogrid pattern matches up along the circumeference. Because the pattern needs to line up around the circular direction of the cone, there are only select values that will pattern so that the pattern is continuous. This is why small changes in this value will likely not affect the overall conical isogrid pattern

### <a id="point-direction-offset-reference"></a>6) Hole Diameter

Hole diameter is an approximate value for the diameter of the cutting holes. This is only an approximate value because the diameter will change as the loft goes closer to the center of the sphere

### <a id="point-angle-offset-reference"></a>7) Arc Radius

Arc radius is an approximate value for the inner radius of the cutting triangles. This is only an approximate value because the radius will change as the cutting loft goes closer to the center of the cone


### <a id="allow-partial-bodies"></a>8) Cut Depth

Cut depth is how far each cutting body will cut into the cone

### <a id="material-thickness"></a>9) Minimum Triangle Height

This is an approximate value for the smallest allowable triangular cut. Because a cone tapers to a point, this feature could keep patterning almost infinitely as the cuts get smaller and smaller. This feature allows you to control what size of triangle the last row of cuts should be

### <a id="hole-to-hole-distance"></a>10) Triangle Height Scale

Because the cone is angled as it gets closer to its point, this can cause some level of distortion that makes the triangles seem shorter or taller than they should be, depending on the angle. This lets you add a multiplier to the height of each row that can make them taller or shorter depending on if this value is greater than or less than one. This should let you correct for this height distortion

### <a id="parameter-definition-type"></a>11) Check for Cuts Close to Edge

Check for cuts close to edge enables "Minimum Distance to Edge" (4) to ensure that all cutting bodies are a certain distance from all edges of the face

### <a id="inside-face"></a>12) Check Edge Mesh Refinement Options

This controls how detailed "Minimum Distance to Edge" (4) should be when checking to make sure that all cuts are a certain distance from each edge

You should pretty much always just leave this on "Rough" and not worry about it, but I wanted to give an option for higher resolution in case anyone wanted it

---

## Tips and General Thoughts

1. conical isogrid is made by creating flat filleted triangles and circles and lofting them towards a point on the axis of the cone. In a perfect world they would be lofted to a line instead of a point, but that ended up not working consistantly so they loft to a point instead. This lofting has two main effects, talked about in points 2 and 3.

2. The first effect of lofting is that the edges of the cuts get distorted if the filleted triangular cuts go around too much of the conical curve. This feature accounts for small amounts of this curved distortion fine, but if the cuts become too relativly large (around more than 8 cuts around the circumference) the pattern will become distorted strangely. This can be overcome with some amount of manual editing outside of this feautre, but the feature will not work by default

3. The second effect of lofting is that as you get closer to the center axis of the cone, the cuts become more spaced out. This becomes important for very deep cuts or if you are using conicals isogrid bodies to cut another non-perfect conical surface (more info on this below)

4. You can use this feature to create conical isogrid bodies to cut other parts. To do this, create a cone a little larger than the surface you want to add isogrid to. Add conical isogrid to this and make the cut depth go as far into the cylinder as needed. Making it cut all the way to the axis can have some weird effects so I recomend adding some buffer there to end the cut depth before it gets all the way to the center. Then create another cone with a hair smaller diameter than the first one (to let you select both bodies). Using direct editing "combine", select subtract, select the second cone as the main body, and select the isogrid pattern as the "bodies to combine." Click the check mark and you should be left with conical isogrid cutting bodies. You can do another direct edit combine subtraction to remove these bodies from the surface you wanted to isogrid

5. Because of the way the lofting is done, there are no radial overhangs in the isogrid, which should make it easier to machine. This is true of all the curved isogrid patterns

